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


### C++ 11

If you need C++ 11 features you'll need to switch to GCC 4.8 using the
update-alternatives command:

```
echo 2 | sudo update-alternatives --config gcc
```

Both GCC 4.6 (default) and GCC 4.8 are installed on every virtual machine. The
above command will switch the default version of GCC to 4.8.
