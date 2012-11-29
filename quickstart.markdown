---
layout: default
title: Quick Start Guide
---

This guide will walk you through the minimum steps to build a project with Drone.io.  

* It assumes you'll be using a Free account and creating a Public project.  
* It also assumes you have a source code repository you can use.  If you don't have a repo, then you can always fork one of Drone.io's open source projects, like [routes.go](https://github.com/drone/routes) or [go.stripe](https://github.com/drone/go.stripe).

### Sign In (or Create Account)

You'll need to be signed in with your Drone.io account.  Select "Sign In" or "Create Account".
![Create Account](img/quickstart-account.png)

### Create Project

Create a project by selecting "New Project", then chose a language and repository type.
![Sign-In](img/new-project.png)

Fill in the project name and provide the repository's public URL.
![New Project](img/quickstart-newproject.png)

It should look like the above screenshot.  Click "Create" when you're done.

### Build Settings

You should end up on the build script settings page after creating the project.  If you're not there, then navigate to **dashboard** > **project** > **settings** > **build**

Take a look at the "Commands" section.  These commands should be the same ones you would use to build your project locally (ie on your laptop).  If the default commands are wrong, modify them and save.

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

Once you think the commands are good, hit "Build Now."
![Manual Build Now](img/trigger-now.png)

You should get a message that your build request was received.  Wait a few moments (or longer if you know your code takes a while to compile/test), then check to see what the build output.

View the build output by going to **builds** and selecting the individual build from the list.

There's a chance it fails the first time, but that's OK, it's easy to try again.

Main reasons a build fails:

* Not able to copy/clone the source code
 * Verify the repo URL is correct, and is a public one.  You can view and update repo details at any time under **project** > **settings** > **repository**
* Wrong commands
 * When you first create a project a few default commands are added.  If your project doesn't use these commands, delete them and use the ones you would use when compiling/testing on your local computer.
* Wrong directory
 * Look the "working directory" that's listed.  If your build commands expect something different, you can either add some "cd" commands, or update the repo details to use a different path.
* Missing dependencies
 * You can try to "wget" or "sudo apt-get install" whatever you need.  Just add the commands towards the beginning of your script.  If this doesn't work, or the dependency takes a long time to download and install,  [contact](/contact.html) us and it will get added to the virtual build machine image.
 
At this point you should have been able to kickoff a build and review the output.  If you are not sure what your project's build commands should be, or are getting errors, check out the language-specific guides located on the upper right of this page.  

### Triggering Builds

You can always manually trigger a build by hitting your project's "Build Now" button.

Builds can also be triggered by invoking your project's build hook URL.  This is how most people achieve continuous integration...your repository host can signal Drone.io to start a build every time a new commit is made.

Your project's build URL is available at: **project** > **settings** > **general**
![Manual Build Curl](img/trigger-curl.png)

Update your repository host to make an HTTP POST to this URL whenever you want a build triggered.  If you've never setup a build hook (aka "service hook") with your repo, then read [Triggering Builds](/triggers.html#hook).

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

Add a build status image to your project's website or repo's readme. Check out this <a href="https://github.com/drone/routes#readme" target="_blank">example</a>.  The image link for your project is at **projects** > **settings** > **general**

Follow [droneio@twitter](https://twitter.com/droneio) for news and updates.

