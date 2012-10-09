---
layout: default
title: Quick Start Guide
---

This guide will walk you through the minimum steps to build your project with Drone.io.  It assumes you'll be using a Free account and creating a Public project.

### Create Account

You'll need an account with Drone.io.  Sign in or click "Create Account".
![Create Account](img/quickstart-account.png)

If you have more questions about creating an account, read [Create Account / Sign In](/createaccount.html).

### Create Project

Create a project by selecting "New Project".
![Sign-In](img/new-project.png)

You'll be asked for basic information about your repository; the most important is your repository's URL.  The URL needs to be publicly accessible.

### Build Script

Go to your build settings located at **project** > **settings** > **build**

Hit "Build Now" to see if Drone.io can access your project and build it using default commands.
![Manual Build Now](img/trigger-now.png)

There's a chance it fails the first time, but that's ok.  If it fails you should look at the build output.  First make sure that your source code was successfully copied/cloned from your repository.  If it wasn't then double check your repository URL for typo's, and make sure it's publicly accessible.  If that's not it then look through the more detailed guide: [Create Project & Add Repository](/newproject.html)

If your source code was successfully copied/cloned, but your build failed, then it is because of the build commands.

Review the build commands and make sure they are correct for your project.  You should be able to use the same commands to build and test your project that you are using locally (ie on your laptop).

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
