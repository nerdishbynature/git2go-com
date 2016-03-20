---
layout: post
title: How to manage your Podcast Show Notes with Git
twitter_username: herbigt
categories: blog
---

While the first thing which comes to most people's mind when they think of potential use cases for Git-based version control is probably code-related, there are actually some other cool situations in which you may want to consider using Git for organizing files.
One rather unordinary one recently came to my mind and I’d like to share some insights with you regarding how I adopted a new workflow for another side project of mine.

## Look beyond development for new Git use cases

As I already wrote in [an earlier post][1], my background is by far not necessarily development-related, but I learned to love using Git over time practicing it. 
So, besides writing and [publishing][2] posts like this one for our Jekyll-based site, I decided to also organize all related documents around the [Productish podcast][4] which I host with my pal [Tim Adler][3], on GitHub.

## How we organize our Podcast files on GitHub

Until now, we had simple markdown files in a shared Dropbox folder, but struggled with the collaborative aspect of editing them for every new episode. 

So I moved the files to a private repo as a first step. In total, it now contains 3 files (excluding the read me):
- Our ongoing collection of topics to discuss
- The preparation for a new topic/episode
- The final show notes of an episode you'll read inside Overcast or your podcast app of choice

While we always just edited the documents asynchronously before and had to merge the files by copying the changes into the respective other document, hosting the files on Git offered much more convenience for exactly this challenge.
Even when both of us now start to prepare the next episode or want to pick something from our topic backlog, we can easily avoid interferences through the commit history of our repo.

## Branching out new Episodes

When a new episode approaches, we then just create a new branch for it. Thereby, we have a clear location to look for changes the other one has created in anticipation for what’s coming.  

To avoid a flood of documents for every episode, we now collect preparation and show notes for all episodes in one file but structure it with the Markdown table of contents for a better overview right on top of the document.

	{{TOC}}

During the recording, we then only have to briefly pull the latest changes from one another and have **one** perfectly aligned document to look at.
When the episode is done, up and live, we can merge the respective episode branch into the master and have a new starting point for preparing the next one.

Which other use cases for version control with Git have you already discovered and what do you still struggle with? Let me know on [Twitter][5] or via [e-mail][6]

[1]:	http://git2go.com/blog/2016/03/13/Confessions-of-a-Git-Novice.html
[2]:	https://itunes.apple.com/us/app/git2go-git-client-you-always/id963577401?mt=8
[3]:	http://toadle.me
[4]:	http://productish.com
[5]:	http://twitter.com/herbigt
[6]:	mailto:tmhrbg@gmail.com