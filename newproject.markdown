---
layout: default
title: Create Project & Add Repository
---

This document will explain how to create a new project, and how to hook it up to one of your code repositories. 

It assumes:

* You have created a Drone.io account
* Your source code is in a version control system
* Your repository is hosted and available over the internet.  For example, you could be using GitHub, Bitbucket, Google Code, etc. 


## Create a Project


### Add a Project
Click the "New Project" button, it's located in the upper right.

![Sign-In](img/new-project.png)

Next you need to select the main programming language of your project, and the type of version control system you repository uses. 
Currently the following repository types are supported:

* Git (git)
* Mercurial (hg)
* Bazaar (bzr)
* Subversion (svn)

### Provide Repository Details

You will need to enter a name for your project, provide the url of your repository, and decide what level of access to give other users.

![Sign-In](img/new-repo.png)

The repository url is the most critical field.  The url will be different depending on the type of version control system and where it's hosted.  Here are some common examples:
<table>
<tr><th>Repo Type</th><th>Host</th><th>Valid Url</th></tr>
<tr><td>Git (git)</td><td>Github</td><td>git://github.com/bradrydzewski/routes.go.git</td></tr>
<tr><td>Git (git)</td><td>Bitbucket</td><td>git@bitbucket.org:bradrydzewski/ipython.git</td></tr>
<tr><td>Bazaar</td><td>Self hosted on EC2</td><td>bzr+ssh://ubuntu@ec2-50-19-200-219.compute-1.amazonaws.com/~/src/node-demo</td></tr>
</table>

To finish creating the project, click "Create."

### Enable Drone.io to Access to your Repository 

If your repository is publicly available, then you're all set to start building and can skip the rest of this guide.  Read more about [configuring](/buildscript.html) and [triggering builds](/triggers.html).

If your repository is private, then you will need to update your repository host to allow Drone.io to checkout your code.  This is done by adding your Drone.io project's SSH key to your host's list of allowed keys.

A Drone.io project's SSH key is located under **project** > **settings** > **keys**

![Deployment Key](img/deploy-key.png)

Here are the instructions for adding your project's drone.io key to some common hosts:

* [Github](/github.html#keys)
* [Bitbucket](/bitbucket.html#keys)

After you adding the key you should be all set to start building.  Read more about [configuring](/buildscript.html) and [triggering builds](/triggers.html).
