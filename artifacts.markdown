---
layout: default
title: Build Artifacts
---
Drone can be configured to archive files generated during your builds.
To setup your build artifacts, go to the  **project** > **settings** > **artifacts** page.

Enter the paths of the files that you would like to archive in the text box,
separated with newlines:

![Artifacts](img/screenshot_artifacts.png)

**IMPORTANT:** these paths should be *relative to* your source repository's root directory.

Drone also supports Globs (pattern matching) to archive files. For example,
`bin/*.zip` will archive all zip files in your repositories `bin` folder.

Build artifacts can be downloaded from **project** > **downloads**

![Downloads](img/screenshot_downloads.png)
