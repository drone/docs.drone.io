---
title: SSH Deployments
layout: default
---

This document covers Continuous Deployment to custom servers using **SSH** and
**rsync**. Here is the configuration screen for SSH deployments:
![Deployment Setup](img/screenshot_deployments_ssh.png)

## User and Host

SSH connects and logs in to the specified hostname (or IP address) using the
specified user account. **NOTE:** your user account must be configured with
passwordless authnetication (using an SSH Key).

## Remote Path

The location on the server where your entire project will be copied. Drone will
copy your entire repository, including any files generated during your build
(i.e. your war file). **IMPORTANT:** make sure this directory exists on your remote
server, and the user id has write priveleges.

## Remote Commands

Commands that will be executed on your remote server. When executing these
commands, the working directoy is set to the *Remote Path*.

Let's assume the *Remote Path* was set to */home/ubuntu/temp*, which is where
your project is copied. You might use the following remote commands:

```sh
#stop nginx
/usr/bin/nginx -s stop

# remove existing app
rm -rf /www/myapp

# copy your app to the deployment directory
mkdir /www/myapp
cp -pr /home/ubuntu/temp/* /www/myapp

# start nginx back up
/usr/bin/nginx -s start
```

## Branch <small>Optional</small>

If the Branch filter is empty, Drone will execute your deployment for all
branches. If you only want certain branches to automatically deploy, you can
specify them in this field as a comma-separated list.

## Authorization

You will need to add the SSH Deploy Key to your server's `.ssh/authorized_keys`
file. You can get the ssh key by clicking the **Show Deployment Key** button.







