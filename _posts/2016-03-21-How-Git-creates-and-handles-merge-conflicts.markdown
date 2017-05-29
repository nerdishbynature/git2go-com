---
layout: post
title: How Git creates and handles merge conflicts
twitter_username: pietbrauer
categories: blog
readtime: 7 min read
---

What is a merge conflict? What does actually happen when you run into a merge conflict? And how do you get rid of it? This blog post intends to answers all your questions and offers advice as well as in-depth Git knowledge.

Wether you are an iOS developer that has to handle Xcode project file merge conflicts or a blogger who collaborates with other writers on articles, there is a good chance you run into them once in a while: merge conflicts. No one really likes them and I think it's Git's most hated state to be in. But once you get familiar with them you may find it interesting how you got there, how to produce a merge conflict or how to prevent it and most importantly how to solve them and move on.

## How to produce a merge conflict

Before we dig into on how to produce a merge conflict we first have to define what a merge conflict actually is. Git makes it easy to handle branches and the changes in them. When you combine two branches it is called a merge. You can see this when you make a PullRequest on GitHub or just merge your feature branch into your master/development branch. There are two types of merges Git can perform:

- __Fast forward__: This is the easiest one, you simply made some commits on your feature branch and nothing big happened on your base branch (e.g. master). Git takes all the commits you made on your feature branch and puts them on top of your base branch. No extra commits are made and no merge conflicts arise.
- __A merge with a merge commit__: You may have seen this commit around `Merge branch 'feature/my-feature' into 'master'`. This is a real merge commit, combining two branches into one. This commit specifies which 2 commits SHAs are being merged and is written on top of your base branch. This state can go well, like it does when you do a PullRequest or it can result in a merge conflict leaving it to the user to resolve the conflicts and proceed with the merge. Once you finished resolving the conflicts, you commit the files and Git prepopulates the commit message for you.

Knowing what we are looking for we have to find out how to reproduce a merge conflict. To do that we prepared a video showing you the actions in our app `Git2Go`:

<iframe title="YouTube video player" class="youtube-player" type="text/html" 
width="640" height="390" src="https://www.youtube.com/embed/EDqihknoLJg"
frameborder="0" allowFullScreen></iframe>

Since I have no intention to change the `master` branch we create a new branch called `branch1` off of this branch we create a new branch called `branch2`. You would normally create these two from your base branch with the intention to merge them into it later on. It might not even be you creating both of them but a collaborator.
Next we modify the `README.md` on `branch1`. We commit the changes and switch to `branch2` where we also modify `README.md`. Since we changed the same lines on both files we think it might be a better idea to combine these changes into one branch only. So we check out `branch1` and merge `branch2` into it and are greeted with an alert message that displays the files affected and a short description of what just happened. It leaves us with a conflicted file and it is now up to us to resolve it.

![Merge conflict Alert]({{ site.url }}/img/2016-03-25-merge-conflict-alert.jpg)

## What Git did under the hood

Before we get to solving the merge conflict we want to take an in-depth look at what was just created for us. We know that Git is file based and all states will be written to some file in the `.git` directory of your repository. We know that because we can reboot our computer, move the repository and the merge conflict will still be there. It is not an in-memory state. When we implemented merge conflict support for [Git2Go][1] we needed to understand how Git does it and how to achieve it using [`libgit2`][2].

We had and solved merge conflicts for years but there is a big difference between using Git and implementing Git functionality yourself, so we did what every sane person would have done and created a merge conflict on our computer and drew a diagram on a white board:

![merge conflicts diagram]({{ site.url }}/img/2016-03-25-merge-conflicts-diagram.png)

When you merge a commit into your current branch and Git cannot resolve the conflict it aborts the merge and writes four files to the `.git` directory:

1. `.git/MERGE_HEAD`: A plain text file containing *their* `HEAD` that you want to merge into your branch, e.g. `9dabbe824510fea810526cbd67cd34e0905ac21f`
2. `.git/ORIG_HEAD`: This text file contains *your* `HEAD` that your branch is currently pointing at
3. `.git/MERGE_MODE`: A file containing the way the merge should be performed, this is usually empty of contains your merge preferences, e.g. `-no-ff` indicating that you want a merge commit and it should not be fast-forwarded.
4. `.git/MERGE_MSG`: This file is interesting because it contains the populated message that should be used when you finished resolving your conflicts. This contains something like:

```
Merge commit '9dabbe824510fea810526cbd67cd34e0905ac21f'

Conflicts:
	README.md
```

5. `README.md`: last but not least Git writes the merge markers to the file(s) that conflicted. In our case:

```bash
<<<<<<< HEAD
ruby
$ jekyll serve
=======
bash
$ jekyll serve -w -something-else
>>>>>>> 9dabbe824510fea810526cbd67cd34e0905ac21f
```

Having been given all these files, we can later determine how the merge should be done, which two commits are involved and what the merge strategy and message will be.
A commit has usually only one parent - the commit before the current commit - but a merge has two parents indicating the merge so your coworkers and friends can see which commits you combined into one. The merge message also contains the conflicted files so all contributors can see which files were affected and how you solved the conflict.

## How to resolve a merge conflict

When we have look at the `README.md` we see lines like this:

![merge conflict markers]({{ site.url }}/img/2016-03-25-merge-conflicts-markers.jpg)

The arrows are so called merge conflict markers. Markers with arrows pointing to the left are the start of a merge conflict, markers with equal signs divide the two versions and markers with arrows pointing to the right mark the end of the merge conflict.

Next to the start and end markers are the two heads you try to merge. `HEAD` is the most recent commit on the branch you are currently on and `9dabbe824510fea810526cbd67cd34e0905ac21f` is the commit that caused the merge to fail. Knowing all this resolving the conflict is pretty easy: Just decide which is the desired outcome for your merge it is:

```
$ jekyll serve -something-else
```

And all you have to do is to delete the lines you don't want to have and delete the markers. When you are done, head to the status and add all files. Once you press "commit" you are greeted with a message like:

![merge conflicts commit message]({{ site.url }}/img/2016-03-25-merge-conflicts-message.jpg)

This message was populated of `libgit2` for us and all that's left to us is to hit commit without modifying it. And voila we get a nice merge commit added to our history which combined both commits.

Watch the full video here:

<iframe title="YouTube video player" class="youtube-player" type="text/html" 
width="640" height="390" src="https://www.youtube.com/embed/DlEzknUFnRY"
frameborder="0" allowFullScreen></iframe>

I hope you enjoyed this explainer of this 'popular' Git state. If so, feel free to share it with your Git-affiliated friends and us up [on Twitter ][3]with your merge conflict experiences - possibly even from an iOS device.

[1]:	https://git2go.com/
[2]:	https://github.com/libgit2/libgit2
[3]:	http://twitter.com/Git2Go