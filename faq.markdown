---
layout: default
title: FAQ - Frequently Asked Questions
---

## Frequently Asked Questions

### How much does it cost for Open Source projects?

There is a free tier for open source projects.  There are a few limits on the free tier, but the majority of open source projects shouldn't be hitting the limits.  Please contact us if you have an open source project that is running into the limits.

### I have multiple branches.  How do I limit which branches trigger a build?

There is a branch filter you can set.  Go to **project** > **settings** > **repository**. By default any branch that's changed will trigger a build. You can limit builds to only happen for specific branches by adding them here. Separate the branch names with a comma. Example: master, ver1.0, dev

### How do I build a project that depends on multiple private repositories?

You can add your Drone.io project level key as a user key on your source code host.  The Drone.io project key is on **project** > **settings** > **repository**. Click the "View Key" button.  Take that key then add it to your version control host at the user level.

### Do I have to use the "Build Now" button to trigger a build?

No, you don't have to use the "Build Now" button.  The most common way to enable continuous integration is to have your repository invoke your projects build url whenever a change is committed.  This should happen automatically for projects hosted on GitHub or Bitbucket.  To set this up on a custom repo, take a look at the guide [Triggering Builds](/triggers.html).

### I'm using a postgres database. How do I create a role?

Use the following command and swap out "yournamehere" with whatever you want:

```
createuser -s yournamehere -U postgres
```

<!-- 
How do I use the build status images / badges?
Is Drone.io an open source project?
I can't get my project to successfully build.  What should I do?
-->




