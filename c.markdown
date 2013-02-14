---
layout: default
title: C / C++ Projects
tagline: Building C / C++ Projects
---

The virtual machine is pre-installed with the following software:

* gcc
* clang
* ia32-libs
* make
* autoconf
* automake
* cmake
* scons
* libtool
* build-essential
* libssl-dev

Please note that Virtual Machines run 64-bit Linux, however, ia32-libs are included
if you want to compile for 32-bit.

### Dependencies

You can use **sudo apt-get** to install any dependencies. Note that **sudo** is
configured to execute without a password, and **apt-get** is configured to
execute without prompting the user to continue.

```
sudo apt-get install intltool
```

### Build and Test

By default, your C / C++ project is configured to execute your build with the
following script:

```
./configure
make
make test
```

You may need to change the default build configuration based on your project's
build lifecycle.
