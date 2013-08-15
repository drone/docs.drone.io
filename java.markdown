---
layout: default
title: Java
tagline: Building Java Projects
icon: java
---

The following Java versions are available to your build:

 * OpenJDK 6
 * OpenJDK 7
 * Sun JDK 8

## Build Tools

The following Java build tools are pre-installed:

* Maven
* Ant

## Gradle

If you are using Gradle as your build tool, we recommend using gradle wrapper
by including the gradlew script in your repository and invoking as part
of your build script. Learn more about gradlew here:
[http://www.gradle.org/docs/current/userguide/gradle_wrapper.html](http://www.gradle.org/docs/current/userguide/gradle_wrapper.html)


--------------------------------------------------------------------------------

## Examples

### Example 1

Example build script using maven to build and test your project:

```
mvn install -q -DskipTests=true
mvn test
```
