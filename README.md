# libctru - CTR User Library

Library for writing user mode ARM11 code for the 3DS (CTR)

This library aims to provide the foundations necessary to write 3DS Homebrew, and straightforwardly access the different functionalities provided by the 3DS operating system.
It is not meant to provide higher level functions; to put things in perspective, the purpose of libctru would be to sit between the OS and a possible port of SDL rather than replace it.

The purpose of this fork of ctrulib is to clean up handling of code which is userland, but not an application -- such as system modules and applets.
It is not intended to replace ctrulib in any way. The aim is to reduce repetition and replacements commonly used in these contexts while staying as vanilla as possible.

# Setup

libctru is just a library and needs a toolchain to function. devkitARM (created by [devkitPro](http://devkitpro.org)) is the officially supported ARM cross compiling toolchain, which provides the framework necessary to supply a usable POSIX-like environment, with working C and C++ standard libraries; as well as the tools required to compile homebrew in the 3DSX format, and assemble GPU shaders. The use of other ARM toolchains is severely discouraged.

The most recent version of devkitARM (r46 at the time of writing) is always recommended. The installers/setup scripts supplied by devkitPro install a prebuilt copy of the latest stable version of libctru, which is recommended for general use. Please note that devkitPro has a policy of keeping legacy code to a minimum, so a library upgrade may result in older code failing to compile or behave properly. Developers are encouraged to keep their code working with the latest versions of the tools and libraries.

You may find instructions on how to install devkitARM on [the devkitPro Wiki](http://devkitpro.org/wiki/Getting_Started).

# Documentation

The documentation is automatically built upon release and can be found at the following url: [http://smealum.github.io/ctrulib](http://smealum.github.io/ctrulib)

# License

  This software is provided 'as-is', without any express or implied
  warranty.  In no event will the authors be held liable for any
  damages arising from the use of this software.

  Permission is granted to anyone to use this software for any
  purpose, including commercial applications, and to alter it and
  redistribute it freely, subject to the following restrictions:

  1. The origin of this software must not be misrepresented; you
     must not claim that you wrote the original software. If you use
     this software in a product, an acknowledgment in the product
     documentation would be appreciated but is not required.
  2. Altered source versions must be plainly marked as such, and
     must not be misrepresented as being the original software.
  3. This notice may not be removed or altered from any source
     distribution.

This fork contains some additional code, which is under different licenses:

fsreg.c, fsreg.h, pxipm.c, pxipm.h - Originates from @yifanlu's 3ds_injector.

The MIT License (MIT)

Copyright (c) 2016 Yifan Lu

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
