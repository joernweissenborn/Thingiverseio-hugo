
---
aliases:
- /doc/installing/
lastmod: 2016-01-04
date: 2013-07-01
menu:
  main:
    parent: getting started
next: /overview/usage
prev: /overview/quickstart
title: Installing thingiverseIO
weight: 20
---

ThingiverseIO is mainly written in [Go][] and currently runs on Linux and Windows. Support for OSX is possible, but hasn't been implemented yet.

You can find the latest release at [ThingiverseIO Releases](https://github.com/ThingiverseIO/thingiverseio/releases).
We currently provide pre-built binaries for
<i class="fa fa-windows"></i>&nbsp;Windows
and <i class="fa fa-linux"></i>&nbsp;Linux,
supporting x64, i386 and ARM architectures.

ThingiverseIO can also be compiled from source wherever the Go compiler tool chain can run, e.g. for other operating systems including DragonFly BSD, OpenBSD, Plan&nbsp;9 and Solaris.  See http://golang.org/doc/install/source for the full set of supported combinations of target operating systems and compilation architectures.

However, for compiling you need [ZeroMQ](https://zeromq.org/).

Under Linux, your should be able to install it via your distributions package manager. You will most likely need the development version of the package, e.g. 'zeromq-dev(el)'.

Also [GCC](https://gcc.gnu.org/) is required. Windows users can either use [MinGW](http://www.mingw.org/), [tdm-gcc](http://tdm-gcc.tdragon.net/) or [Cygwin](https://www.cygwin.com). Cygwin provides precompiled binaries for zeromq, which simplifies compilation.

## Installing ThingiverseIO (binary)

  TBW

## Upgrading Hugo

TBW


## Installing from source

### Prerequisite tools for downloading and building source code

* [Git](http://git-scm.com/)
* [GCC](https://gcc.gnu.org/)
* [Go][] 1.5+ (Windows users must wait for 1.7, since building c-archives will only be supported from this release on. However, you can compile Go from the latest sources.)

### Get ZeroMQ

If available on your platform, you can use your package manager to get ZeroMQ. You will need the the headers as well, so install the development version, e.g. 'zeromq-dev'. Make sure that the provided version is 4.x, otherwise you need to install it from source.

If you are on Linux, you can install it from source following [these instructions](http://zeromq.org/intro:get-the-software). 

On Windows, you can not use the provided binaries, since they are build using the MSVC toolchain, which is not compatible with Go. You need to use [MinGW](http://www.mingw.org/), [tdm-gcc](http://tdm-gcc.tdragon.net/) or [Cygwin](https://www.cygwin.com).
With Cygwin, you can download zeromq-devel with the package manager.

Look [here](https://stackoverflow.com/questions/24138558/how-to-build-zeromq-with-mingw) for more detailed instructions. Warning: the [offical documention]() is outdated

### Get directly from GitHub

    $ export GOPATH=$HOME/go
    $ go get -v github.com/spf13/hugo

`go get` will then fetch Hugo and all its dependent libraries to your
`$GOPATH/src` directory, and compile everything into the final `hugo`
(or `hugo.exe`) executable, which you will find sitting in the
`$GOPATH/bin/` directory, all ready to go!

You may run `go get` with the `-u` option to update Hugo's dependencies:

    $ go get -u -v github.com/spf13/hugo

## Contributing

Please see the [contributing guide](/doc/contributing/).

[Go]: http://golang.org/
