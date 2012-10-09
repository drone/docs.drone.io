---
layout: default
title: Go
tagline: Building Go Projects
icon: golang02
---

The following Go versions are available to your build:

 * Go1 (stable)

## Go Path

When compiling your Go program, it is important that your repository is cloned
to the path that matches your Go program's full package name or desired binary
name.

When creating your project we will attempt to automatically set your checkout
path based on the name and URL of the source repository:

![Go Path](img/screenshot_golang_build-path.png)

You can change the default checkout path at the
**project** > **settings** > **repository** page.

## Dependencies

Use the **go get** command to install your project's dependencies:

```
go get code.google.com/p/codesearch/index
go get github.com/petar/GoLLRB/llrb
```

## Build

Use the **go build** command to compile your code:

```
go build
``` 

## Test

Use the **go test** command to run unit tests:

```
go test -v
```

You may use alternative unit test frameworks, such as [gocheck](http://labix.org/gocheck):

```
go get launchpad.net/gocheck
go test -gocheck.v
```
--------------------------------------------------------------------------------

## Examples

### Example 1

Example build script for [web.go](https://github.com/hoisie/web), a lightweight
web framework written in Go.

The project build path is automatically set to `github.com/hoisie/web`

```
go get
go build
go test -v
```

### Example 2

Example build script for [jkl](https://github.com/bradrydzewski/jkl), a
Jekyll-based static site generator written in Go.

The project build path is automatically set to `github.com/bradrydzewski/jkl`

```
go get
go build
go test -v
```

We can optionally archive the **jkl** binary that is generated during the build.
For more information, please see the [build artifact documentation](/archive.html).
