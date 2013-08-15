---
layout: default
title: Build Environment
---
The following environment variables can be used to identify your current
environment as a build server:

* `CI=true`
* `DRONE=true`

The following environment variables can be used to query meta data about
the currently running build:

* `DRONE_REPO_SLUG`: the name of your project (github.com/:user/:repo)
* `DRONE_BUILD_URL`: the url of your build (drone.io/github.com/:user/:repo/:build)
* `DRONE_BUILD_DIR`: the location of your code and working directory of your build script
* `DRONE_BUILD_NUMBER`: the current build number
* `DRONE_COMMIT`: the commit hash currently being built
* `DRONE_BRANCH`: the branch currently being built

The following environment variables can be used for
[Jenkins compatibility](https://wiki.jenkins-ci.org/display/JENKINS/Building+a+software+project):

* `JOB_NAME`: the name of your project (github.com/:user/:repo)
* `WORKSPACE`: the location of your code and working directory of your build script
* `BUILD_URL`: the url of your build (drone.io/github.com/:user/:repo/:build)
* `BUILD_DIR`: the location of your code and working directory of your build script
* `BUILD_ID`: the current build number
* `GIT_COMMIT`: the commit hash currently being built
* `GIT_BRANCH`: the branch currently being built
* `SVN_REVISION`: the revision number currently being built

