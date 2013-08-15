---
layout: default
title: Branches
---

When you setup your Github or Bitbucket repository, Drone
will automatically configure a post-commit hook. This allows Github and
Bitbucket to automatically trigger a build every time you commit code.

When Github and Bitbucket trigger builds, they provide metadata about your
commit, including the *branch*. Drone will always execute your build for
your commit's branch:

```
git checkout -b your_branch git@github.com/your_repo
```

Just to reiterate ... you should not checkout a branch as part of your
build script. Drone will do this automatically.

## Excluding Branches

Drone will build any branch specified in the post-commit hook (excluding gh_pages).
If you want Drone to ignore certain branches, you will need to setup a **Branch
Filter**.

Go to your project's **settings** > **repository** page. In the Branch Filter
text box you can specify a comma-separated list of Branches that are eligible
for builds. All other Branches are ignored.

![Branch Filter](img/screenshot_repo_settings_branches.png)

In the above screenshot, only changes to the "master" and "prod" branches
will trigger a build.
