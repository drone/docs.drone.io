---
layout: default
title: Scala
icon: scala
tagline: Building Scala Projects
---

The following Scala versions are available to your build:

* Scala 2.8.2
* Scala 2.9.2

## Java Version

The Scala Virtual Machines are configured to use OpenJDK6. If you would
prefer OpenJDK7 you can add the following command to your build script:

```
sudo update-java-alternatives -s java-1.7.0-openjdk-amd64
```

### Testing

By default, Scala tests are run using SBT:

```
sbt ++2.9.2 test
```

### Dependencies

If you are using SBT, all dependencies will be automatically retrieved when
executing the **sbt test** command. Alternatively, **maven** is also available
to manage your project's build lifecycle.
