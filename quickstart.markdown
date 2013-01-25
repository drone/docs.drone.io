---
layout: default
title: Quick Start Guide
---

This guide will walk you through the minimum steps to build a project with Drone.io.  

* It assumes you'll be using a Free account and creating a Public project.
* It also assumes you have a source code repository you can use.  If you don't have a repo, then you can always fork one of Drone.io's open source projects, like [routes.go](https://github.com/drone/routes) or [go.stripe](https://github.com/drone/go.stripe).

### Sign In (or Create Account)

You'll need to be signed in with your Drone.io account.  Select "Login" or "Sign up."
![Create Account](img/quickstart-account.png)

### Create Project

Create a project by selecting "New Project" then pick the site your repo is on.
![Sign-In](img/new-project.png)

Select your repo from the list.
![List](img/repo-list.png)

### Build Settings

Select your language then confirm your build script.  These commands should be the same ones you would use to build your project locally (ie on your laptop).  If the default commands are wrong, modify them and save.

Some example build commands for projects with standard setups:

Builds Commands ([Dart](/dart.html)):

```
pub install
test/run.sh
```

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

### Build Now

Your project is now setup to automatically build when your source code changes.  You can also manually trigger a build whenever you want.  This is very useful for debugging build issues or for trying out new features.

Just hit "Build Now."
![Manual Build Now](img/trigger-now.png)

You should get redirected to your build's realtime output.

View any of you build's output by going to **History** and selecting the individual build from the list.

There's a chance it fails the first time, but that's OK, it's easy to try again.

Main reasons a build fails:

* Incorrect build commands
 * When you first create a project a few default commands are added.  If your project doesn't use these commands, delete them and use the ones you would use when compiling/testing on your local computer.
* Wrong directory
 * Look the "working directory" that's listed.  If your build commands expect something different, you can either add some "cd" commands, or update the repo details to use a different path.
* Missing dependencies
 * You can try to "wget" or "sudo apt-get install" whatever you need.  Just add the commands towards the beginning of your script.  If this doesn't work, or the dependency takes a long time to download and install,  [contact](/contact.html) us and it will get added to the virtual build machine image.
 
At this point you should have been able to kickoff a build and review the output.  If you are not sure what your project's build commands should be, or are getting errors, check out the language-specific guides located on the upper right of this page.  

### The End

Congratulations! You just setup and built a project with [Drone.io](https://drone.io). A great place to go next is one of the language-specific guides:

* [C](/c.html)
* [C++](/cpp.html)
* [Dart](/dart.html)
* [Go](/golang.html)
* [Java](/java.html)
* [Node.js](/node.html)
* [Python (Beta)](/python.html)
* [Ruby (Beta)](/ruby.html)

To archive your build artifacts read [Archiving Files & Build Artifacts](/artifacts.html).

To configure notifications review [Notifications](/notifications.html).

If you want to automate deployments look at [Deployments](/deployment.html) or jump to the the [Heroku](/heroku.html) or [Dotcloud](/dotcloud.html) guides.

For any issue or concern please [contact](/contact.html) us.

### Extra Credit

Add a build status image to your project's website or repo's readme. Check out an <a href="https://github.com/drone/routes#readme" target="_blank">example</a>.  

The image link for your project is at **settings** > **status badges**.

![Badge](img/badge-info.png)

Follow [droneio@twitter](https://twitter.com/droneio) for news and updates.

