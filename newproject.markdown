---
layout: default
title: Project Setup
---
This guide will walk you through the minimum steps to setup your Github or
Bitbucket repository to automatically build, test and deploy you code using
[drone.io](https://drone.io).

This guide assumes the following pre-requisites:

* You have Bitbucket or Github account
* You [created](https://drone.io/register) a Drone account
* You own or administer at least one public Github or Bitbucket repository

## Setup your Project

Login to Drone and click on the **New Project** button in the upper-right
corner of your screen:
![Dashboard](img/screenshot_dashboard.png)

Pick where your source code is hosted:
![Host](img/screenshot_repo_setup_hosts.png)

Select your repository from the list:
![List](img/screenshot_repo_setup_list.png)

Select the main programming language for your project:
![Lang](img/screenshot_repo_setup_lang.png)

The last step is to double check the build commands.  You will see a list of common build and test commands based on the language you choose.  If they look correct for your project, hit "Save" and you're done.  
![Script](img/screenshot_repo_setup_cmds.png)

These build commands can be anything you enter on the command line.  Once you are done making changes, hit "Save."

## Build your Project

To manually trigger a build, click the **Build Now** button:
![Build Now](img/screenshot_repo_setup_buildnow.png)

Your build's console output is streamed real-time to the browser. You can use this
output to troubleshoot your build when you have compiler issues or test failures.

<!--
### Triggering Builds

**drone.io** will automatically add a [post-recieve hook](https://help.github.com/articles/post-receive-hooks)
to your Github project:

> Every GitHub repo has the option to communicate with a web server whenever
> the repo is pushed to. These "WebHooks" can be used to update an external
> issue tracker, <b>trigger CI builds</b>, update a backup mirror, or even deploy
> to your production server.

### Private Repositories

If you project is private, **drone.io** will also add a
deploy key to your repo:

> A deploy key is an SSH key that is stored on the server and grants access
> to a single repo on GitHub. This key is attached directly to the repo
> instead of to a user account.

<a name="bitbucket"></a>
## Bitbucket

### Build Hooks

**drone.io** will automatically add a [service hook](https://confluence.atlassian.com/display/BITBUCKET/Managing+Bitbucket+Services)
to your Bitbucket repo. A service hook is a URL that gets invoked
every time you commit a code change, and instructs **drone.io** to
checkout, build and test your code.

### Private Repositories

If you project is private, **drone.io** will also add a deploy key to your repo:

> A deployment key grants read-only access to a public or private repository.
> With a deployment key a user or a process can pull or clone a repository over
> SSH. <b>Deployment Keys are particularly useful when you need to authenticate
> a build server to checkout and test your code.</b>

<a name="googlecode"></a>
## Google Code

### Build Hooks

In order to setup continuous integration with **drone.io**, you should add
a [Post-Commit Hook](https://code.google.com/p/support/wiki/PostCommitWebHooks)
to your project settings:

> Post-Commit Web Hooks allow projects to setup web services that receive
> project commit notifications from Google Code. Such services could be used
> to integrate external tools including <b>continuous build systems</b>,
> bug trackers, project metrics, and social networks.

In Drone

In Google Code

-->

## Finished

Congrats! Your project is setup, and a build hook was automatically added to
your Github or Bitbucket repository. Any new changes to your source code will
trigger a build.
