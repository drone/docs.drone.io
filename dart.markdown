---
layout: default
title: Dart
---

The following Dart versions are available to your build:

* Dart SDK
* Dart SDK (Continuous / Nightly)

The DART_SDK environment variable is available and included in the PATH:

```
export DART_SDK=/usr/local/dart-sdk
export PATH=$PATH:$DART_SDK/bin
```
The following Dart command line tools are available:

* Dart-to-JavaScript compiler (dart2js)
* Dart VM (dart)
* Dart package manager (pub)


### Dependencies

The Dart SDK includes a package management utility called [Pub](http://www.dartlang.org/docs/pub-package-manager/).
Executing **pub install** will download all dependencies defined in the **pubspec.yaml** file.

```
pub install
```

## Examples

Example build script for the [html5lib](https://github.com/dart-lang/html5lib)
project maintained by Google's [Dart team](https://github.com/dart-lang):

```
pub install
tests/run.sh
```

Real-world Dart projects using [drone.io](https://drone.io):

* [kevmoo/bot.dart](https://drone.io/kevmoo/bot.dart/script/config)
