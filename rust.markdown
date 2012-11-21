---
layout: default
title: Rust
---

The virtual machine is pre-installed with **Rust 0.4** and includes the following
binaries in the the user path:

 * rustc
 * rustdoc
 * cargo

## Builds

The default build script for each Rust project is the following:

```
make
make test
```

You will likely want to edit this build script to meet the specific needs of
your project. If you do not use a Makefile you can invoke the Rust compiler
directly:

```
rustc myprogram.rs
```

## Dependencies

The **cargo** utility is available for managing Rust dependencies:

```
cargo install sdl
cargo install central/sdl
cargo install git://github.com/brson/rust-sdl
cargo install http://example.com/pkg.tar.gz
```

## Tests

By default your tests are executing using the `make test` command. If you do not
use a Makefile you can generate and execute your tests in your build script:

```
rustc myprogram.rs --test -o myprogram-tests
./myprogram-tests
```
