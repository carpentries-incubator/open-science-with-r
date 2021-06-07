---
title: "Version control with git"
teaching: 45
exercises: 45
questions:
- "What is version control? How do I use it?"
- "What is the difference between `git`and Github?"
- "What benefits does a version control system brings in for my research?"
objectives:
- "Understand the benefits of using a version control system such as `git`."
- "Be able to decipher git jargon: repository, commit, push, pull, branches etc."
- "Understand the basics of `git` and its usage in RStudio."    
keypoints:
- "In a version control system, file names do not reflect their versions."
- "`git` acts as a time machine for files in a given repository under version control."
- "`git` allows you to test changes and discard them if not relevsant."
- "A new RStudio project can be smoothly integrated with `git` to allow you to version control scripts and other files."
---


## Table of contents
<!-- MarkdownTOC autolink="True" levels="1,2,3" -->

- [1. Introduction](#1-introduction)
    - [1.1 What is a version control system and why scientists should use it?](#11-what-is-a-version-control-system-and-why-scientists-should-use-it)
    - [1.2 Five reasons to use a version control system in research](#12-five-reasons-to-use-a-version-control-system-in-research)
    - [1.3 What is git?](#13-what-is-git)
- [2. Working on your own with git](#2-working-on-your-own-with-git)
    - [2.1](#21)
    - [A good commit message](#a-good-commit-message)
- [3. GitHub online](#3-github-online)
- [4. Integration of RStudio with git and GitHub](#4-integration-of-rstudio-with-git-and-github)
    - [4.1 Set-up](#41-set-up)
- [5. Exercise: write a paper on your own](#5-exercise-write-a-paper-on-your-own)
    - [5.1 Major determinants of life expectancy](#51-major-determinants-of-life-expectancy)
    - [5.2 Add dataset and make a figure](#52-add-dataset-and-make-a-figure)
    - [5.3 add commit push](#53-add-commit-push)
    - [5.4 Make changes to the figure](#54-make-changes-to-the-figure)
    - [5.5](#55)
- [Going further](#going-further)

<!-- /MarkdownTOC -->

# 1. Introduction

In this episode, you will learn about the `git` version control system and how to use it in your project. We will see how to link your local `git` folder to a remote on the internet, using the GitHub platform to host our code and text files. Finally, we will see how RStudio can manage all these operations as part of a RStudio project.

> ## Important note
> In this episode, code will broadly refer to all sorts of scientific outputs you can create with a computer such as:
> A script written in R to create a publication figure. 
> A script written in Python that produces a statistical analysis from a dataset. 
> A master script that calls external functions and other script to perform a full-fetched analytical workflow.
{: .callout}

## 1.1 What is a version control system and why scientists should use it?

In the context of a research project, a version control system will help you to manage your project history, progress and support active collaboration with your colleagues but also with you (past, present and future self).  

As a concrete example, this is something we might have all experienced in the past when keeping track of file versions:

![](../img/MessySaves.png)

![](../img/phdcomics_version_control.png)

Version control will help you to avoid this file nightmare but also fosters other good scientific practices. 

## 1.2 Five reasons to use a version control system in research

1. __Tell the story:__ The history of your commit messages will describe your project progress.
2. __Travel back in time:__ a version control system makes it easy to compare different time points of your project smoothly. If you want to compare the stage of your project a year ago from now, it only takes one command-line of code. 
3. __Experiment with changes:__ if you want to make changes in a script, you can first make a "snapshot" of the project status before experimenting with changes. As a researcher, this might be a second nature for you! 
4. __Backup your work:__ by being able to linking your local repository (folder) to a distant online host, a version control system backs up your precious work instantly.
5. __Collaborate easily on projects:__ having a web-hosted synchronised version of your project will encourage collaboration with other researchers. Think about a colleague of yours being able to add a script to make a figure for your first PhD publication for instance.  

There are possibly other important reasons why you could use a version control system for your research project. While originally created for software development, a common usage in scientific research is to track versions of datasets, scripts or figures easily and efficiently.

## 1.3 What is git?

> ## Definition
> Defined simply: 
> `git` is an application that runs on your computer like a web browser or a word processor (Tom Stuart).   
{: .callout}

Git is a _version control system_ primarily used in software development. 
<img src="../img/07-git-logo.gif" width="400px" alt="git logo">


In 

# 2. Working on your own with git

## 2.1 


## A good commit message 

1. Separate subject from body with a blank line
2. Limit the subject line to 50 characters.
3. Capitalize the subject line.
4. Do not end the subject line with a period.
5. Use the imperative mood in the subject line.
6. Wrap the body at 72 characters.
7. Use the body to explain what and why vs. how. The how is self-explainable from your code. 


Major commands: 
# 3. GitHub online 

GitHub is a company 
Git + Hub = a website that hosts your project work, its history and nurture collaborations with your peers.  

But much more! It has dozens of features that makes version control easier and more appealing. 

| GitHub jargon                                                                                 | human translation                                                                                                                                         |
|--------------------------------------------------------------------------------------------   |---------------------------------------------------------------------------------------------------------------------------------------------------------  |
| user: A   Github account for you (e.g., jules32).                                             | a Github account for you (e.g., jules32).                                                                                                                 |
| organization:   The Github account for one or more user (e.g., datacarpentry).                | the Github account for one or more user (e.g., datacarpentry).                                                                                            |
| repository:   A folder within the organization that includes files dedicated to a project.    | a folder within the organization that includes files dedicated to a   project.                                                                            |
| clone                                                                                         | process of making a local copy of a remote Github repository. This only   needs to be done once (unless you mess up your local copy).                     |
| pull                                                                                          | copy changes on the remote Github   repository to your local Github repository. This is useful if multiple people   are making changes to a repository.   |
| push                                                                                          | save local changes to remote Github                                                                                                                       |

# 4. Integration of RStudio with git and GitHub

The RStudio https://support.rstudio.com/hc/en-us/articles/200532077-Version-Control-with-Git-and-SVN

## 4.1 Set-up

# 5. Exercise: write a paper on your own

## 5.1 Major determinants of life expectancy

## 5.2 Add dataset and make a figure

## 5.3 add commit push

## 5.4 Make changes to the figure

## 5.5  

# Going further

- [A "git for humans" presentation](https://inbo.github.io/git-course/static/presentations/git.pdf)
- Jenny Bryan's [HappyGitWithR](http://happygitwithr.com) is very useful for troubleshooting, particularly the sections on [Detect Git from RStudio](http://happygitwithr.com/rstudio-see-git.html) and [RStudio, Git, GitHub Hell (troubleshooting)](http://happygitwithr.com/troubleshooting.html).
- [Online game](https://learngitbranching.js.org/)
- [RStudio webinar on GitHub and RStudio](https://rstudio.com/resources/webinars/managing-part-2-github-and-rstudio/)
- [Using git and GitHub for scientific writing](http://paulklemm.com/blog/2014-07-16-use-github-for-scientific-writing/)