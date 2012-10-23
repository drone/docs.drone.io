---
layout: default
title: Trigger a Build
---

<a name="manual"></a>
## Manual Builds

There are two ways to trigger a manual build.  

The first way way is to go to your project's settings page and select "Build Now."

![Manual Build Now](img/trigger-now.png)

The second way to trigger a manual build is to make a web request POST to your project's build URL using your local computer. Your project's manual build url is located under **project** > **settings** > **general**

![Manual Build Curl](img/trigger-curl.png)

If you are a linux user, then this is very easy to do with the cUrl utility.  The exact command syntax can be found along with your build URL on **project** > **settings** > **general**

Here is another example:

```
curl -X POST http://www.drone.io/tdburke/routes.go?key=76e4asdsdasd232323sae776c75c1b742bad97
```

<a name="hook"></a>
## Continuous Builds

Many users want will want their projects to build automatically when a commit is made to their repository.

This is enabled by setting up a "build hook" on your repository host.  A build hook makes a basic web request POST to your Drone.io project's build URL.  Your project's build URL is located on **project** > **settings** > **general**

![Manual Build Curl](img/trigger-curl.png)

Builds hooks are sometimes called "Service Hooks" or simply "Services", and setting them up varies slightly depending on the site hosting the repository.

Here are detailed guides for setting up a Drone.io build hook on popular hosts:

* [Github](/github.html#hooks)
* [Bitbucket](/bitbucket.html#hooks)


