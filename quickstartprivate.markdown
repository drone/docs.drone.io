---
layout: default
title: Quick Start Guide
---

This guide will walk you through the minimum steps to build your project with Drone.io.

### Create Account

You'll need an account with Drone.io.  Sign in or click "Create Account".
![Create Account](img/quickstart-account.png)

If you have more questions about creating an account, read [Create Account / Sign In](/createaccount.html).

### Create Project

Create a project by selecting "New Project". You'll be asked for basic information about your repository; the most important is your repository's URL.

If your repository is public, you can [jump to the next section](#build-script) to configure your build.

If your repository is private, you'll need to add your Drone.io project's **SSH key** as a deploy key to your repo host (like Github or Bitbucket).

If you've never done this before, or run into any issues, read [Create Project & Add Repository](/newproject.html)

Your Drone.io project's deploy key is located under **project** > **settings** > **keys**
![Deployment Key](img/deploy-key.png)

### <a id="build-script"></a>Build Script

Go to your build settings located at **project** > **settings** > **build**

To verify that Drone.io can access your repository, hit "Build Now" for the project you just created.
![Manual Build Now](img/trigger-now.png)

This will trigger a build that gets your code and tries to build it based on the most common defaults for the programming language you selected.  If this fails because it can't get a copy of your code, verify that you followed all the steps in [Create Project & Add Repository](/newproject.html) 

Review the build commands and make sure they are correct for your project.

Some examples for projects with standard setup:

Builds Commands ([Java](/java.html)):

```
mvn install -q -DskipTests=true
mvn test
```

Builds Commands ([Python](/python.html)):

```
pip install -r requirements.txt --use-mirrors
nosetests
```

Builds Commands ([Go](/golang.html)):

```
go get
go build
go test -v
```

If you are not sure what your project's build commands should be, or you are getting errors when you trigger builds, check out the language-specific guides located on the upper right of this page.

### Trigger Builds

You can always manually trigger a build by hitting your project's "Build Now" button.

You can also set up a build hook on your repository host to tell Drone.io to start a build every time a new commit is made.

If you've never setup a build hook (aka "service hook") with your repo, then read [Triggering Builds](/triggers.html#hook).

Your project's build URL is available at: **project** > **settings** > **general**
![Manual Build Curl](img/trigger-curl.png)

After a build completes, you can see its output by clicking on the build in your project's "Builds" section. 

### Next Steps

Congratulations! You just set up your first Drone.io project. A great place to go next is one of the language-specific guides:

* [Dart](/dart.html)
* [Go](/golang.html)
* [Java](/java.html)
* [Python](/python.html)

To automate your deployments, read [Deployments](/deployment.html) or jump to the the [Heroku](/heroku.html) or [Dotcloud](/dotcloud.html) guides.

To archive your build arifacts, read [Archiving Files & Build Artifacts](/artifacts.html).

To configure notifications, read [Notifications](/notifications.html).

The full list of guides is available here: [Documentaion](/..).
