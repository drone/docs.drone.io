---
title: Heroku Deployments
layout: default
xlogo: "img/heroku-logo-light-300x100.png"
---

This document covers Continuous Deployment to Heroku using [drone.io](http://drone.io)

This document assumes:

* You are registered for a Heroku account
* You installed the [Heroku Toolbelt](https://toolbelt.heroku.com) on your computer
* You have created an application using `heroku create`

## Register SSH Key

You will need to register your project's deployment key with Heroku. This will
enable the build server to connect to Heroku and deploy your application.

Download your SSH key from the Heroku page, then execute the `heroku keys:add` command:

```sh
$ heroku keys:add my-project-key.key
Uploading SSH public key my-project-key.key... done
```

## Deployment Setup

Once your project's deployment key is registered, setup auto-deployment to
Heroku by providing your application's git repository:

![Deployment Setup](img/screenshot_deployments_heroku.png)

## Build Output

Next time your project build executes you should see the following output:

```
$ git remote add heroku git@heroku.com:my-hello-world-app-6685.git
$ git push heroku master
Warning: Permanently added 'heroku.com,50.19.85.156' (RSA) to the list of known hosts.

-----> Heroku receiving push
-----> Python app detected
-----> Preparing Python interpreter (2.7.2)
-----> Creating Virtualenv version 1.7.2
       New python executable in .heroku/venv/bin/python2.7
       Also creating executable in .heroku/venv/bin/python
       Installing distribute.........................................done.
       Installing pip................done.
       Running virtualenv with interpreter /usr/local/bin/python2.7
-----> Activating virtualenv
-----> Installing dependencies using pip version 1.1
       Downloading/unpacking Flask==0.7.2 (from -r requirements.txt (line 1))
       Creating supposed download cache at /app/tmp/repo.git/.cache/pip_downloads
       Successfully installed Flask Werkzeug Jinja2
       Cleaning up...
-----> Discovering process types
       Procfile declares types -> web
-----> Compiled slug size is 3.7MB
-----> Launching... done, v3
       http://nameless-meadow-6685.herokuapp.com deployed to Heroku

To git@heroku.com:my-hello-world-app-6685.git
 * [new branch]      master -> master
```

