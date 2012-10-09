---
layout: default
title: Configuring a Build Script
---

## Select Language

The first step is choosing your project's language. Selecting a language determines
which type of virtual machine executes your build, and ensures the virtual machine
is configured correctly:

![Choose a Language](img/build-language.png)

## Build Script

The next step is to setup environment variables and enter you build commands:

![Choose a Language](img/build-script.png)

### Working Directory

Your builds working directory is `/home/ubuntu/src`. If you entered an optional
checkout path, then your builds working directory is `/home/ubuntu/src/your/checkout/path`.

## Post-Build

### Notifications

Configure your build to send email notification upon completion by
entering email addresses (commma separated) into the "Emails" text box.

Email notifications will be sent to all recipients for both Successful and
Failed builds.

![Choose a Language](img/build-archive-notify.png)

### Archives

Configure your build to archive files for download. In order to
flag a file for download, enter the **relative file path** (relative to your
project's working directory) into the "Build Archives" text box.

Examples:

* `bin/myproject.zip` will archive the file `/home/ubuntu/src/bin/myproject.zip`
* `bin/*.zip` will archive all zip files in `/home/ubuntu/src/bin/`

Build artifacts may be downloaded from **project** > **downloads**

![Archive Binary](img/file-archive-2.png)

## Limits

The following limits are placed upon all builds:

* a build cannot exceed 15 minutes
* a build cannot notify > 5 email recipients
* a build cannot archive > 5 files
* archived files cannot exceed 10 MB

