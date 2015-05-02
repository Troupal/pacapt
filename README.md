## NAME

`pacapt` - An `Arch`'s pacman-like package manager for some `Unices`.

## DESCRIPTION

An `Arch`'s pacman-like package manager for some `Unices`.
Actually this `Bash` script provides a wrapper for system's package manager.

Instead of remembering various options/tools on different `OS`s, you only
need a common way to manipulate packages. Not all options of the native
package manager are ported; the tool only provides a very basic interface
to search, install, remove packages, and/or update the system.

`Arch`'s pacman is chosen, as pacman is quite smart when it divides all
packages-related operations into three major groups:
  `Synchronize`, `Query` and `Remove/Clean up`.
It has a clean man page, and it is the only tool needed to manipulate
official packages on system.
(`Debian`, for example, requires you to use `apt-get`, `dpkg`, and/or `aptitude`.)

The tool supports the following package managers:

* `pacman`        by `Arch Linux`, `ArchBang`, `Manjaro`, etc.
* `dpkg/apt-get`  by `Debian`, `Ubuntu`, etc.
* `homebrew`      by `Mac OS X`
* `macports`      by `Mac OS X`
* `yum/rpm`       by `Redhat`, `CentOS`, `Fedora`, etc.
* `portage`       by `Gentoo`
* `zypper`        by `OpenSUSE`
* `pkgng`         by `FreeBSD`
* `cave`          by `Exherbo Linux`
* `pkg_tools`     by `OpenBSD`

## INSTALLATION

1. This script shouldn't be installed on an Arch-based system.
2. On `FreeBSD`, please install `bash` package first
3. Use the stable script

````
$ wget -O /usr/local/bin/pacapt \
    https://github.com/icy/pacapt/raw/ng/pacapt
$ chmod 755 /usr/local/bin/pacapt
````

This scrip is actually picked from the latest stable branch,
which is `v2.0` at the moment. If you want to compile a script
from its components, please make sure you use a correct branch.
See `CONTRIBUTING.md` for details.

## DEVELOPMENT

A development version

````
$ git clone https://github.com/icy/pacapt.git
$ cd pacapt

# switch to development branch
$ git checkout ng

# compile the script
$ ./compile.sh > pacapt.dev

# check if syntax is good
$ bash -n pacapt.dev

$ install -m755 ./pacapt.dev /usr/local/bin/pacapt
````

Please read the sample `Makefile` for some details.

## USAGE

After installing `pacapt` script, you can get help message by

    $ pacapt -h # or pacapt --help

## SUPPORT

Please use the ticket system at https://github.com/icy/pacapt/issues .

## AUTHORS

* 10sr
* Alexander Dupuy
* Anh K. Huynh
* Arcterus
* Cuong Manh Le
* Danny George
* Darshit Shah
* Hà-Dương Nguyễn
* Huy Ngô
* James Pearson
* Karol Blazewicz
* Konrad Borowski
* Somasis
* Vojtech Letal
