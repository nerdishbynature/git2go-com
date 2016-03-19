---
layout: post
title: How to manage your Podcast Show Notes with Git
twitter\_username: herbigt
categories: blog
---

While the first thing which comes to most people's mind when they think of potential use cases for Git-based version control is probably code-related, there are actually some other cool situations in which you may want to consider using Git for organizing files.

## Look beyond development for new Git use cases
As I already wrote in [an earlier post][1], my background is by far not development-related, but I learned to love using Git. So, besides writing and [publishing][2] posts like this one for our Jekyll-based site, I decided to also organize all related documents around the Productish podcast, which I host with my pal [Tim Adler][3], on GitHub.

## How we organize our podcast files on GitHub 
Until now, we had simple markdown files in a shared Dropbox folder, but struggled with the collaborative aspect of editing them for every new episode. 

So I moved the files to a single private repo as a first step. In total, it contains 3 files (excluding the read me):
- Our ongoing collection of topics to discuss
- The preparation for a new topic/episode
- The final show notes of an episode you'll read inside Overcast or your podcast  app of choice


[1]:	http://git2go.com/blog/2016/03/13/Confessions-of-a-Git-Novice.html
[2]:	https://itunes.apple.com/us/app/git2go-git-client-you-always/id963577401?mt=8
[3]:	http://toadle.me