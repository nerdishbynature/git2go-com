---
layout: post
title: Git for writing scientific papers and theses
twitter_username: kallenbergjulia
categories: blog
---

I wish I had known about git and its opportunities while writing the final thesis for my university studies.

When I wrote my final thesis a few years ago, I had heard about git but only in the context of saving different versions of code. So I never even considered it helpful in the matter of writing a scientific paper. Looking back, I know now that my life could have been so much easier in many ways.

## Backups

I saved my backups on different USB sticks and external hard drives. Since my thesis included many diagrams and images, each copy needed quite some space. So I filled up directories and external storage media with copies.
Also, it was kind of hard to keep track which external hard drive actually contained which version. While trying to clean up the whole mess at some point, I managed to delete my latest version. Don’t ask me how that happened, but it definitel was not intended. Luckily, it was still stored in iCloud, but you can imagine how close I was to a heart attack at that point.

Git providers have remote servers so your documents will always be stored in their cloud and you don’t need to worry about ten different hard drives to keep your paper save. Github, being one of the most well-known providers, even offers a free plan for students.

## Versions and Changes

In order to keep track of the evolution of the document, I kept saving new versions marked with the date of the latest changes. But to be honest, I hardly went back to actually look at the changes from one version to another. It’s just too much hassle going back forth between huge documents.

Git on the other hand shows you side by side changes you have made, what has been added by whom, what has been changed and what has been deleted. This way, you are way less tempted to change the same sentence back and forth. 

## Chapters

One of the first things you need to do when you start writing your thesis is to structure it in logic chapters. To make your life easier you could make use of another option git allows you to do. You could create a branch for each chapter. Whenever you finish the next chapter you can merge the chapter branch to your master branch so you know what has been. The temptation of doing a bit here and there is quite high especially in the beginning, you can just do what feels at the moment, but this way it easy to lose track. Working on one chapter after the other is much more structured approach.

## Reworking

I am sure everybody who has ever written a complex paper (mine ended up having about 120 pages all together) knows how hard it is to keep track on the parts that you may have checked and double checked already, and whenever you go back, you will find pieces that you want to change, since for whatever reason they don’t feel quite right to you anymore. 

As you have an overview of the changes you have made, reworking drafts is also easier since you know what you have done already and therefor from where to continue. This saves a lot of your time.

## Reviewing

When writing your thesis you will ususally get to the point where you have people proof reading it for you. They can then make pull requests with their suggestions for changes and you can decide if you want to go with them or not - either merge them or just close them.

You will know exactly where to look for suggested changes instead of digging through a whole paper mountain.

## Collaborating

Git is also great for group work, since it is one of its major purposes in the 'tech world'. You can add contributors to a project who then can make changes to the content. The most common issue with group work in the conventional sense is to always provide the latest version to all team members. 
With git there is no need to send updated versions via email amoung the group members anymore. You get notified about updates and can comment on changes or contribute to the latest version. 
If different contributors have added changes at the same time there is no straight forward way to merge all changes in one document. Git will show where you have conflicting updates and you can simply choose which change you want to take to the next stage.
To lern more about the handling of conflicts you can also check out our article on merge conflicts. [Add Link]

You can not only commit your changes directly to the repository but you can also create pull requests instead so that the other team members can review your changes and merge them if they agree.

In order to make use of all the advanteages git has to offer you just need to use a git compatible editor.
I wrote my thesis in Pages for Mac and the option of showing diffs doesn’t work with Pages. I suspect it wouldn’t work with Word documents either, but git does for example work with LaTex, which is quite common to use for writing scientific papers.
You can basically use any markdown editor and it will support the full set of git features. 
I have come to like Ulysses a lot for its clean design, the document analytics and the options to export it in many different document types. I mainly use it for writing blog articles but it handles especially large documents very well.

As you see, git in combination with a text editor has the ability to ease many common troubles when writing complex papers.
This article is focused on writing a scientific paper but all the above mentioned applies to any kind of complex editorial work and contribution, of course.

With Git2Go you can make or look at changes while commuting or lying on the couch with your iPhone or iPad.

