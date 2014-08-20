go-build
========

`go-build` is compile and install different versions of Go on UNIX-like systems.

# Requirements

~~~~
curl
gcc
git
hg
make
~~~~

# Installation

## Default

~~~~
$ curl -s https://raw.githubusercontent.com/tkuchiki/go-build/master/install-go-build | bash
~~~~

## Change install dir

Set `GOBUILD_ROOT` and `GOBUILD_BIN`.

~~~~
$ curl -s https://raw.githubusercontent.com/tkuchiki/go-build/master/install-go-build | \
  GOBUILD_ROOT=/path/to/gobuild_root GOBUILD_BIN=/path/to/gobuild_bin bash
~~~~

# Command

~~~~
$ go-build
Usage: go-build

Options:
    init     initialize go-build
    install  install go
    versions display versions
    upgrade  upgrade go repository
~~~~

# Usage

## Initialize

Execute hg clone.

~~~~
$ go-build init
~~~~

## Install go

Install a specify version and directory.

~~~~
$ go-build go1.3.1 /opt/go/1.3.1
~~~~

## Show versions

Show stable and rc, beta versions.

~~~~
$ go-build versions
~~~~

Show all versions.

~~~~~
$ go-build versions all
~~~~~

## Upgrade go repository

Upgrade go repository.

~~~~
$ go-build upgrade repo
~~~~

Upgrade go-build.

~~~~
$ go-build upgrade self
~~~~