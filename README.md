

# INBO Git workshop

## Introduction

At INBO, people do write code and require version control. As `git` is not the most straightforward environment to work with for non-IT specialists, we try to define our own sub-ecosystem with relevant practices and an achievable workflow.

In this repository, we collect the material for workshops and courses given by/for INBO people, but for other interested researchers/... as well. 

A workshop typically takes a whole day, with the morning session focused on getting the concepts and terminology clear and an afternoon hands-on session.

## Workshop content

### Morning session

We explain the main terminology of Git based on 5 important tasks:

1. Tell the story of your project 
1. Travel back in time
1. Experiment with changes
1. Backup your work
1. Collaborate on projects

The morning session is provided using slideshows, split in two main sections:

* [Git](static/presentations/git.pdf)
* [GitHub](static/presentations/github.pdf) 

We like to thank Alice Bartlett, as her `git-for-humans` talk, https://speakerdeck.com/alicebartlett/git-for-humans was a major source of inspiration to the course material.

### Afternoon session

The content of the hands-on session in the afternoon depends on the audience of the workshop. Most of the people mainly work in Rstudio and it makes sense to use the integrated git-tools of Rstudio. Others are used to work in the command line or prefer Github Desktop to handle version control. As such, we have three similar sessions, targeted at the different audiences:

* Using Git with [RStudio](course_rstudio.html)
* Using Git with GitHub Desktop (old presentation not yet converted)
* Using Git with the command line (old presentation not yet converted)

## Setup

In order to follow the git-course, the main installation requirement is [git](https://git-scm.com/) itself. Further configuration is explained during the tutorial. 

For the git through RStudio, an installation of R and Rstudio is expected as well. For the Github Desktop version, an installed version of [Github Desktop](https://inbo.github.io/git-course/).

## Course development note

The course is written as a combination of `.md` and `.Rmd` files (in `src`) and rendered using the `rmarkdown` package. Rendering the course webpage can be done using the command (assuming an Rstudio project in the main repo folder):

```r
rmarkdown::render_site("src")
```

And the resulting `html` pages are updated to the `docs` folder. The `docs` folder of the master is used to [deploy the Github pages](https://help.github.com/articles/configuring-a-publishing-source-for-github-pages/#publishing-your-github-pages-site-from-a-docs-folder-on-your-master-branch).

The source for the Git and GitHub presentations are Google Presentations by @stijnvanhoey and @peterdesmet. In the directory `slideshow`, there are a number of presentations not yet converted to course pages.
