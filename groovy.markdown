---
layout: default
title: Groovy
tagline: Building Groovy Projects
---

The following Groovy versions are available to your build:

 * Groovy 2.0
 * Groovy 2.1

## Java Version

The groovy Virtual Machines are configured to use OpenJDK6. If you would
prefer OpenJDK7 you can add the following command to your build script:

```
sudo update-java-alternatives -s java-1.7.0-openjdk-amd64
```

### Gradle

Gradle is installed and available for your build. Most groovy projects
will use the following standard commands in their build script:

```
gradle assemble
gradle check
```

Maven and Ant are also installed and available for use in your build script.
