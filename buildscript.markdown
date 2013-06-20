---
layout: default
title: Build Commands
---

## Select Language

Choose your project's programming language. Selecting a language determines
which type of virtual build machine executes your build, and ensures the virtual machine
is configured correctly:

![Choose a Language](img/build-language.png)

## Build Script

Add environment variables (optional), databases (optional), and enter your build commands (required):

![Build Commands](img/build-script.png)

### Working Directory

Your project's working directory is `/home/ubuntu/src`. If you entered an optional
checkout path, then the working directory is `/home/ubuntu/src/your/checkout/path`.

## Limits

The following limits are placed upon all builds:

* a build cannot exceed 15 minutes (free tier only)
* a build cannot notify > 5 email recipients
* a build cannot archive > 5 files
* archived files cannot exceed 10 MB

If you need a limit changed, please [contact](/contact.html) us.

