---
layout: default
title: Integrating with Github
logo: "img/github.png"
---

<a name="keys"></a>
## Adding Deploy Keys

If your repository is public, then you don't need to add a deploy key.  If it's private, then continue reading.

Click on the "Admin" tab of repository's home page.  To add a deploy key click on "Deploy Keys" in the left hand menu, then hit the "Add Deploy Key" button..

![Github Deploy Key](img/github-deploykey.png)

You will need to paste in your Drone.io project's SSH deploy key.  If is found in Drone.io under **project** > **settings** > **keys**

Once you paste the key into Github, give the key a name, and then click "Add Key."

Drone.io will now be able to checkout your code when a build is triggered.

<a name="hooks"></a>
## Adding Build Hooks

Github can trigger an automatic build every time you make a commit to your repository.  This is done using a "Service Hook."  A Github service hook is just a plain web request using POST with your Drone.io project's url.

To add a service hook, click on the "Admin" tab of repository's home page, then choose "Service Hooks" in the left hand menu.

All available service hooks are listed on this page.  You need to choose "Web Hook URLs", which is at the top of the list. 

![Github Build Hook](img/github-hook.png)

You will need to copy your Drone.io project's build url into Github's WebHook URL field.

Your Drone.io project's build hook url is found under **project** > **settings** > **general**

Once you copy this url into Github, click "Update Settings."

From this point on any commits to your repository should trigger a build of your project on Drone.io.

Note: It is recommended to trigger a build manually before adding a automatic build hook.  Instructions for triggering manual builds are [here](/triggers.html#manual)

