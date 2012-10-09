---
layout: default
title: Java
tagline: Building Java Projects
icon: java
---

The following Java versions are available to your build:

 * OpenJDK 6
 * OpenJDK 7

## Build Tools

The following Java build tools are pre-installed:

* Maven
* Ant

--------------------------------------------------------------------------------

## Examples

### Example 1

Example build script using maven to build and test your project:

```
mvn install -q -DskipTests=true
mvn test
```
