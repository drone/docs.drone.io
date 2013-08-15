---
layout: default
title: Haskell
tagline: Building Haskell Projects
---

The following Haskell versions are available to your build:

 * Haskell 7.4 (official debian package)
 * Haskell 7.6

## Dependency Management

You can execute the following cabal command to install you dependencies:

```
cabal install --only-dependencies --enable-tests
```

## Build and Test

You can execute the following cabal commands to build and test your code:

```
cabal configure --enable-tests && cabal build && cabal test
```

Please note: your build commands are fully customizable. If you prefer, you can
always invoke a Makefile or shell script to build and test your code.

--------------------------------------------------------------------------------

## Examples

### Example 1

Example build script using cabal:

```
cabal install --only-dependencies --enable-tests
cabal configure --enable-tests && cabal build && cabal test
```
