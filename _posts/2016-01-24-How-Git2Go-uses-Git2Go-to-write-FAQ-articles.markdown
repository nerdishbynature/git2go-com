---
layout: post
title: How Git2Go uses Git2Go to write Git2Go FAQ articles
twitter_username: pietbrauer
categories: blog
---

Let's admit it: managing and writing documentation or FAQ articles is the most boring thing on earth and as a small team of two it is too time consuming. Maybe one day we will have an intern program where people write a lot of FAQ articles but for now we are stuck with ourselves. So how to make it fun and get multiple purposes out of the task?

When we first started the FAQ [someone made the wise decision](https://github.com/nerdishbynature/git2go-faq-web/commit/c878687f107e45c50ba1d31ced7cfb386e426121) to use Jekyll as its backbone. In case you don't know: [Jekyll](http://jekyllrb.com) is a static website/blogging system written in Ruby that you can use for your website or blog. Articles are written in markdown (which we love) and the source can be managed in Git (which we also like, obviously). If you are interested in our FAQ system you can have a look at the repository on GitHub: [https://github.com/nerdishbynature/git2go-faq-web](https://github.com/nerdishbynature/git2go-faq-web) .

When Git2Go was not yet released we used our MacBooks to start the FAQ blog and write the first articles. We believe that an FAQ should not be too excessive but to be crisp and clear. We have a very good support system where we usually answer within the first hour ([Read more about it here](http://building.git2go.com/2016/01/09/05-35-33-Support.html)). If we get a lot of support requests for a specific topic we decided to write a support article. As I said, in the past we had to switch to our Macs to do so, but since we try to transition to mobile only users, we wanted to use iOS for our FAQ too. To do this we sat together with some bloggers. Notably Alex from [Hipsterpixel](http://hipsterpixel.com) was the biggest help and he showed us his mobile only workflow, which he uses to write his blog while he is commuting. He liked our app very much and so we realized some of his ideas.

## How we write a new FAQ article

### Creating the Jekyll scaffold

The most tedious task when writing a Jekyll article is getting the header right. As we don't need any SEO or categories that is easily automated using [Workflow](https://workflow.is/). We found a good workflow on the Internet and modified it using workflow. You can download the workflow we use [here](https://workflow.is/workflows/c1b3bc3cecaa48898d06e2381df104a0).  It is simply asking you for a title, grabs the current date, encodes all the components and opens the generated text in [1Writer](http://1writerapp.com/). Of course you can extend it like Alex did for SEO improvements and category support.

### Writing the article and submitting

For writing the article we use 1Writer, an app which can handle iCloud and has a very cool USP: it has support for URL based quick actions. When we are finished writing the article we want it to be saved in Jekylls `_posts/` directory. We could use the document provider extension introduced in Git2Go v1.5 but that would mean:

1. Share the text
2. Choosing Git2Go
3. Navigating to the `_posts` directory
4. Dropping the article there

These are 4 steps, which means doing this every time we write a FAQ article is a very repeating task. As a programmer I don't like that, so [we integrated URL schemes](http://faq.git2go.com/2016/01/24/How-to-use-URL-schemes.html) in Version 1.5 of Git2Go, too.

This means you can have an action like the following setup for your blog in 1Writer and publishing it is just a tap away.

![OneWriter Share Action]({{ site.url }}/img/2016-01-24-OneWriter.jpg)

Let's have a look at the URL from the action `gittogo://repositories/github/nerdishbynature/faq/files/new?content=[text]&path=_posts/[name]`. We choose the current repository to be the FAQ repository with the article's content and the name appended to the `_posts` path. This will open Git2Go and write the post's contents to the path. You can then go ahead and commit the changes to your file and push it to the remote.

### Hosting

For hosting we just use [GitHub Pages](https://pages.github.com) which is a free service from GitHub. They will use Docker images to generate the static websites that Jekyll is producing and host them for you. The upsides of this approach is, that we don't have to worry about hosting a server and if we get some traction GitHub will handle it as well.

## Conclusion

Writing Support articles solely on iOS helps us get to know the iOS eco system even better, explore other people's workflows and test our own app in the wild. It also helps us getting to know our users and maybe show more ways on how to use our app and make them more productive on their iOS devices.

**All the actions described here use Git2Go 1.5 which will be released on January 25.**
