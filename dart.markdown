---
layout: default
title: Dart
---

The following Dart versions are available to your build:

* Dart integration (from https://gsdview.appspot.com/dart-editor-archive-integration)
* Dart bleeding_edge (from https://gsdview.appspot.com/dart-editor-archive-continuous)
* Dart trunk (from https://gsdview.appspot.com/dart-editor-archive-trunk)

The DART_SDK environment variable is available and included in the PATH:

```
export DART_SDK=/usr/local/dart-sdk
export PATH=$PATH:$DART_SDK/bin
```
The following Dart command line tools are available:

* Dart-to-JavaScript compiler (dart2js)
* Dart VM (dart)
* Dart package manager (pub)
* Dart Analyzer (dart_analyzer)

## Dependencies

The Dart SDK includes a package management utility called [Pub](http://www.dartlang.org/docs/pub-package-manager/).
Executing **pub install** will download all dependencies defined in the **pubspec.yaml** file.

```
pub install
```

## Testing

At this time, Dart does not have a standard build management tool (ie maven).
So you will probably need to modify the default build script to ensure your
tests are executed correctly.

For further instruction, please see the build Script [documentation](/buildscript.html).

## Headless Browser Tests

A headless verion of webkit, **DumpRenderTree**, it also available for testing
your client-side code. To use DumpRenderTree you will need to start **xvfb** (a virtual xwindows system)
in your build script:

```
sudo start xvfb
```

For an example project using DumpRenderTree, see the Dart team's
[web-ui](https://github.com/dart-lang/web-ui) project.

## Handling Dart Releases

The Dart team releases a new version of the SDK about once every week.
Drone offers a feature called **Triggers** to proactively build and test your
project every time a new version of the dart-sdk is released.

To enable this Trigger, go to your Project **Settings > Triggers**:

![Proactive Dart Builds](img/screenshot_triggers_dart.png)

## Examples

Example build script for the [html5lib](https://github.com/dart-lang/html5lib)
project maintained by Google's [Dart team](https://github.com/dart-lang):

```
pub install
test/run.sh
```

Real-world Dart projects using [drone.io](https://drone.io):

* [dart-lang/pop-pop-win](https://github.com/dart-lang/pop-pop-win)
* [dart-lang/web-ui](https://github.com/dart-lang/web-ui)
* [kevmoo/bot.dart](https://drone.io/kevmoo/bot.dart/script/config)
