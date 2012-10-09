---
layout: default
title: Build Artifacts
---
Drone.io can be configured to archive files generated during your builds.
To setup your build artifiacts, go to the  **project** > **settings** > **artifacts** page.

Enter the paths of the files that you would like to archive in the text box,
separated with newlines:

![Notifications](img/screenshot_artifacts.png)

**IMPORTANT:** these paths should be *relative to* your source repository's root directory.
