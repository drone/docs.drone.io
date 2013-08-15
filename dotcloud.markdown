---
title: Dotcloud Deployments
layout: default
xlogo: "img/dotcloud.png"
---

This document covers Continuous Deployment to Dotcloud using [drone.io](http://drone.io)

This document assumes:

* You are registered for a Dotcloud account
* You installed the [Dotcloud CLI](http://docs.dotcloud.com/0.9/firststeps/install/) on your computer
* You have created an application using `dotcloud create`
* Your project has a `dotcloud.yml` file checked-in to the repository

## Dotcloud Key

First you need your dotcloud key. Login to your dotcloud account and go to the
[settings](https://account.dotcloud.com/settings) screen.

![Dotcloud API Key](img/dotcloud-key.png)

## Deployment Setup

Setup auto-deployment to DotCloud by providing your API Key and application name:

![Dotcloud API Key](img/screenshot_deployments_dotcloud.png)

## Build Output

Next time your project build executes you should see the following output:

```
$ dotcloud push my-hello-world-app .
# upload my-hello-world-app ssh://dotcloud@uploader.dotcloud.com:443/my-hello-world-app
# git
Warning: Permanently added '[uploader.dotcloud.com]:443,[184.73.62.194]:443' (RSA) to the list of known hosts.
Counting objects: 4, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 302 bytes, done.
Total 3 (delta 1), reused 0 (delta 0)
To ssh://dotcloud@uploader.dotcloud.com:443/my-hello-world-app
   5adaf64..aaaad6e  master -> master
18:48:29 ---> Deploy of "my-hello-world-app" scheduled for revision git-aaaad6e at 2012-09-05 18:48:29
18:48:29 ---> Building the application...
18:48:29 [www] Build started for revision git-aaaad6e (clean build)
18:48:48 [www] Successfully installed Flask Werkzeug Jinja2
18:48:48 [www] Cleaning up...
18:48:52 [www] Build completed successfully. Compiled image size is 3MB
18:48:52 ---> Application build is done
18:48:52 ---> Initializing new services... (This may take a few minutes)
18:48:52 ---> Using default scaling for service www (1 instance(s)).
18:48:52 [www.0] Initializing...
18:49:10 [www.0] Service initialized
18:49:13 ---> All services have been initialized. Deploying code...
18:49:13 [www.0] Deploying build revision git-aaaad6e...
18:49:18 [www.0] Running postinstall script...
18:49:19 [www.0] Launching...
18:49:21 [www.0] Waiting for the instance to become responsive...
18:49:22 [www.0] Re-routing traffic to the new build...
18:49:23 [www.0] Successfully deployed build revision git-aaaad6e
18:49:23 ---> Deploy finished
18:49:23 ---> Application fully deployed

Deployment finished. Your application is available at the following URLs
www: http://my-hello-world-app-johnsmith.dotcloud.com/

```

