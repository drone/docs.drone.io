---
layout: default
title: New Project
---

This document will explain how to create a new project that automatically builds when your source code is changed. 

It assumes:

* You have created a Drone.io account
* You've linked your GitHub or Bitbucket account

## Add a Project

Click the "New" button located in the upper right.

![Sign-In](img/new-project.png)

Pick where your source code is hosted.

![Host](img/repo-pick.png)

Select your repository from the list.  Public projects are free.  Private projects require you to upgrade your billing plan.

![List](img/repo-list.png)

You'll now be asked to select the main programming language for your project.

![Lang](img/lang-list.png)

The last step is to double check the build commands.  You will see a list of common build and test commands based on the language you choose.  If they look correct for your project, hit "Save" and your done.  

![Script](img/review-script.png)

These build commands can be anything you enter on the command line.  Once you are done making changes, hit "Save."  Send an email to support@drone.io if your not sure how to build your project and we'll help you out.

## Finished

Congrats! Your project is setup, and a build hook was automatically added to your repo.  Any new changes to your source code will trigger a build.

Read more about what options you have during your [build](/buildscript.html).

## Build Status Badge

Now you can add a dynamic build status badge to your homepage.  Check out an <a href="https://github.com/drone/routes#readme" target="_blank">example</a>.  
Just update your repo's Readme.md file or place a link on your website.

![Badge](img/badge-info.png)

