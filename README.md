# accents

Accents: a basic Tiberian Hebrew (biblical) cantillation-mark parser based on BHS electronic edition

Written originally in 2000, but verified to compile and test out OK using recent Ubuntu builds.  A basic Dockerfile sufficient for a build:

> FROM ubuntu:latest
>
> RUN apt-get update \
>     && apt-get install -y bison flex libreadline-dev libc6-dev libfl-dev \
>          wget vim make gcc curl unzip build-essential
## Introduction

   Accents is a tool for parsing/checking the "accents" of
Tiberian-pointed biblical manuscripts, specifically those coded
according to the CCAT/ Michigan-Claremont scheme.  If you are not a
biblical scholar or a classical Hebraist, this won't make much sense,
I know :-).  Write to me at the address given below if want some
background, e.g., if you'd like an introductory bibliography to the
study of biblical Hebrew, or recommendations for books on the
structure of the biblical text.

   Accents is written in ANSI C.  I have not kludged the source for
derelict compilers that still cannot handle void pointers or function
prototypes.  If you want to use Accents on a system lacking an ANSI C
compiler, install GNU cc.  Or use the basic Dockerfile offered above
to create your own image.
## Installation

   The 'configure' shell script attempts to guess correct values for
various system-dependent variables used during compilation.  It uses
those values to create a 'Makefile.'  Finally, it creates a shell
script 'config.status' that you can run in the future to recreate the
current configuration, a file 'config.cache' that saves the results of
its tests to speed up reconfiguring, and a file 'config.log'
containing compiler output (useful mainly for debugging 'configure').

   The file 'configure.in' is used to create 'configure' by a program
called 'autoconf'.  You only need 'configure.in' if you want to change
it or regenerate 'configure' using a newer version of 'autoconf'.

The simplest way to compile this package is:

  1. 'cd' to the directory containing the package's source code and type
     './configure' to configure the package for your system.  If you're
     using 'csh' on an old version of System V, you might need to type
     'sh ./configure' instead to prevent 'csh' from trying to execute
     'configure' itself.

     Running 'configure' takes a few minutes.  While running, it
     prints some messages telling which features it is checking for.

  2. Type 'make' to compile the package.

  3. Optionally, type 'make check' to run any self-tests that come with
     the package.

  4. Type 'make install' to install the programs and any data files and
     documentation.

  5. You can remove the program binaries and object files from the
     source directory by typing 'make clean'.  To also remove the files
     that 'configure' created (so you can compile the package for a
     different kind of computer), type 'make distclean'.

   By default, 'make install' will install the package's files in
'/usr/local/bin', '/usr/local/man', etc.  You can specify an
installation prefix other than '/usr/local' by giving 'configure' the
option '--prefix=PATH'.

## Operation Controls

   'configure' recognizes the following options to control how it
operates.

'--cache-file=FILE'
     Save the results of the tests in FILE instead of 'config.cache'.
     Set FILE to '/dev/null' to disable caching, for debugging
     'configure'.

'--help'
     Print a summary of the options to 'configure', and exit.

'--quiet'
'--silent'
'-q'
     Do not print messages saying which checks are being made.

'--srcdir=DIR'
     Look for the package's source code in directory DIR.  Usually
     'configure' can determine that directory automatically.

'--version'
     Print the version of Autoconf used to generate the 'configure'
     script, and exit.

'configure' also accepts some other, not widely useful, options.


Richard Goerwitz
richard@goerwitz.com

