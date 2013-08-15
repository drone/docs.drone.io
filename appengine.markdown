---
title: Google App Engine Deployments
layout: default
---

This document covers automated deployments to Google App Engine for the
**Python** and **Java** runtimes. Please note this feature is currently
in **Beta**.

![Deployment Setup](img/screenshot_deployments_gae.png)

## Refresh Token

You will need to provide Drone with your App Engine refresh token, in order
to authorize the automated deployments. Refresh tokens can be found in the
*.appcfg_oauth2_tokens* or *.appcfg_oauth2_tokens_java* file in your *$HOME*
directory.

For more information, see the [Python](https://developers.google.com/appengine/docs/python/tools/uploadinganapp#oauth) and
[Java](https://developers.google.com/appengine/docs/java/tools/uploadinganapp#Passwordless_Login_with_OAuth2)
documentation for passwordless deployments.

## Application <small>Optional</small>

Uploads the application using the specified ID. By default, this field is taken
from the *app.yaml* file, however, it can be manually overriden using this field.

## Version <small>Optional</small>

Uploads the application using the specified version. By default, this field
is taken from the *app.yaml* file, however, it can be manually overriden using
this field.

## Branch <small>Optional</small>

If the Branch filter is empty, Drone will execute your deployment for all
branches. If you only want certain branches to automatically deploy, you can
specify them in this field as a comma-separated list.

## Queues, Index, Cron and DOS updates

Automatically deploying changes to Queues, Indexes, Cron or your DOS settings
are not yet supported. If you would like to see these features added please
[contact us](mailto:support@drone.io).
