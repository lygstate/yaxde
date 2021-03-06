# YAXDE

YAXDE is a simple cross-dev environment for bare board systems.

## Features

 - Runs on Linux and MinGW (Mac might also work but not tested).
 - Targets bare-board lightweight applications
 - Easy to use
 - Ada, C++, C and Assembly supported
 - GNU based toolchain
 - Modified BSD License
 - Provides scripts and patch for x-gcc generation (with Ada support)


## Directory Tree Description

 - toolchain: Makefile and scripts to build and install x-toolchains
 - boards: default base path for boards files (start, bsp, ...)
 - libraries: default base path for libraries
 - programs: default base path for user programs
 - rts: ZFP Ada runtimes sources and build Makefile

## LANGUAGES

Supported languages are Ada, C++, C and assembly

### Ada
Zero Foot Print

### C++
no stdlib

### C
no libc


## LICENSES:

### Modified BSD License

All project files are covered by "Modified BSD License" aka "New BSD License" :

Copyright (c) 2013, Stany MARCEL All rights reserved.

Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:

- Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.
- Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.
- Neither the name of the '<'organization'>' nor the names of its contributors may be used to endorse or promote products derived from this software without specific prior written permission.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL <COPYRIGHT HOLDER> BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.

Some other files comes from other projects with different licenses.

### GCC

GCC license is GNU General Public License (version 3 or later) with GCC Runtime Library Exception.

GCC Patches are covered by this license.

### GNAT

GNAT files are covered by GNAT Modified General Public License

GNAT files are not distributed with this project but copied from GCC installation when the RTS is build.

Only system.ads is modified and included in this project as it must be
implemented for each board (see also AdaRuntime).

## TOOLCHAIN and TOOLS

### Installation
Tested on xubuntu 12.10 i686 and x86_64 :

run
```
# sudo make install-deps
# make install-toolchain
```

### TARGETs

#### arm-none-eabi
cortex-m cortex-r cortex-a

#### powerpc-none-elf

#### m68k-none-elf
coldfire only

#### MinGW setups
MS Windows MinGW toolchain must be built under linux.
To cross build a toolchain for mingw from ubuntu 12.10
cd install
make TARGETS="arm-none-eabi powerpc-none-elf m68k-none-elf"

After a very long time get installers in install/builds/i686-pc-mingw32

## TODO
Add avr target support
