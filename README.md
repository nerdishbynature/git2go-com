# Git2Go.com

This is the repository for the Git2Go website. It was built using [Jekyll](http://jekyllrb.com). Each section has different parameters that it needs in order to display correctly. If you want to add a new one check out the attached workflows.

## Installation

```bash
$ gem install jekyll
```

### Running the website locally

```bash
$ jekyll serve -w
```

## Categories for the landing page

|Category|Results in|
|--------|----------|
|features|Features of the App, e.g. Editor|
|makers|Contributors to the app, e.g. Tim|
|testimonials|Good things people way about the app a.k.a 'What others say'|

### Features

When adding a new feature you need to provide the following parameters

|Attribute|Example|Description|
|---------|-------|-----------|
|layout|default|Can be ignored|
|title|"Seamless Git Integration for GitHub, GitHub Enterprise, Bitbucket & GitLab"|Title that is shown above the body of the feature|
|date|2016-03-04 11:53:17 +0800|The current date, newer dates will be sorted above other features.|
|image|"/img/img_commits_smlr.png"|Relative path to the image, will be prefixed with `http://git2go.com`|
|imagewidth|300px|The width of the image|
|imageheight|375px|The height of the image|
|categories|features|Needs to be `features`|

Workflow: https://workflow.is/workflows/a23cdb23029a4bbeb2334c054cc8c916

### The Makers

When adding a new maker you need to provide the following parameters

|Attribute|Example|Description|
|---------|-------|-----------|
|layout|default|Can be ignored|
|title|"Piet Brauer"|The name of the maker|
|date|2016-03-04 11:55:18 +0800|The current date, newer dates will be sorted above other makers.|
|maker_image|"/img/PietPortrait.png"|Relative path to the portrait, will be prefixed with `http://git2go.com`|
|categories|makers|Needs to be `makers`|

Workflow: https://workflow.is/workflows/8ec3f94fb3164c11ab521b62554da964

### What others say

When adding a new Testimonial you need to provide the following parmeters

|Attribute|Example|Description|
|---------|-------|-----------|
|layout|default|Can be ignored|
|date|2016-03-04 11:53:16 +0800|The current date, newer dates will be sorted above other makers.|
|image|"/img/RenzoPortrait.png"|Relative path to the portrait, will be prefixed with `http://git2go.com`|
|author|"Renzo Crisóstomo, iOS Developer at XING"|The Name, Job title and Employer/Reputation of the person|
|categories|testimonials|Needs to be `testimonials`|

Workflow: https://workflow.is/workflows/910250c3eb45413bb39184b396f030d8
