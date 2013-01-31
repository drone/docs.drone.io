---
layout: default
title: Integrating with Bitbucket
logo: "img/bitbucket.png"
---

<a name="keys"></a>
## Adding Deploy Keys

If your repository is public, then you don't need to add a deploy key.  If it's private, then continue reading.

Click on the "Admin" tab of repository's home page.  To add a deploy key click on "Deployment Keys" in the left hand menu.

![Bitbucket Deploy Key](img/bitbucket-deploykey.png)

You will need to paste in your Drone.io project's SSH deploy key.  If is found in Drone.io under **project** > **settings** > **keys**

Once you paste the key into Bitbucket, give the key a name, and then click "Add key."

Drone.io will now be able to checkout your code when a build is triggered.

<a name="hooks"></a>
## Adding Build Hooks

Bitbucket can trigger an automatic build every time you make a commit to your repository.  This is done using a "Service ."  A Bitbucket service is just a plain web request using POST with your Drone.io project's url.

To add a service, click on the "Admin" tab of repository's home page, then choose "Services" in the left hand menu.

The dropdown in the middle of the page lists all possible services.  You will need to select "POST", then "Add Service."  There are a lot of options, so you will need to scroll towards the bottom of the dropdown list to find the "POST" option.

![Bitbucket Hooks](img/bitbucket-hook.png)

You will need to copy your Drone.io project's build url into Bitbuckets's POST URL field.

Your Drone.io project's build hook url is found under **project** > **settings** > **general**

Once you copy this url into Bitbucket, click "Save settings."

From this point on any commits to your repository should trigger a build of your project on Drone.io.

Note: It is recommended to trigger a build manually before adding a automatic build hook.  Instructions for triggering manual builds are [here](/triggers.html#manual)


