# GLEW - The OpenGL Extension Wrangler Library

![](http://glew.sourceforge.net/glew.png)

http://glew.sourceforge.net/

https://github.com/nigels-com/glew

[![Build Status](https://travis-ci.org/nigels-com/glew.svg?branch=master)](https://travis-ci.org/nigels-com/glew)
[![Gitter](https://badges.gitter.im/nigels-com/glew.svg)](https://gitter.im/nigels-com/glew?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge)

## Downloads

Current release is [1.13.0](https://sourceforge.net/projects/glew/files/glew/1.13.0/).
[(Change Log)](http://glew.sourceforge.net/log.html)

Sources available as 
[ZIP](https://sourceforge.net/projects/glew/files/glew/1.13.0/glew-1.13.0.zip/download) or
[TGZ](https://sourceforge.net/projects/glew/files/glew/1.13.0/glew-1.13.0.tgz/download).

Windows binaries for [32-bit and 64-bit](https://sourceforge.net/projects/glew/files/glew/1.13.0/glew-1.13.0-win32.zip/download).

### Recent snapshots

Snapshots may contain new features, bug-fixes or new OpenGL extensions ahead of tested, official releases.

[glew-20160131.tgz](http://sourceforge.net/projects/glew/files/glew/snapshots/glew-20160131.tgz/download) 
*GLEW 2.0.0 release candidate: Core context support, MX discontinued*

[glew-20151117.tgz](http://sourceforge.net/projects/glew/files/glew/snapshots/glew-20151117.tgz/download)

[glew-20150805.tgz](http://sourceforge.net/projects/glew/files/glew/snapshots/glew-20150805.tgz/download)

## Build

From a downloaded tarball or zip archive:

### Linux and Mac

#### Using GNU Make

##### Install build tools

Debian/Ubuntu/Mint:    `$ sudo apt-get install build-essential libXmu-dev libXi-dev libgl-dev git`

RedHat/CentOS/Fedora:  `$ sudo yum install libXmu-devel libXi-devel libGL-devel git`

##### Build

  $ cd auto
  $ make
  $ cd ..
	$ make
	$ sudo make install
	$ make clean

Targets:    `all, glew.lib, glew.bin, clean, install, uninstall`

Variables:  `SYSTEM=linux-clang, GLEW_DEST=/usr/local, STRIP=`

#### Using cmake

*CMake 2.8.12 or higher is required.*

##### Install build tools

Debian/Ubuntu/Mint:   `$ sudo apt-get install build-essential libXmu-dev libXi-dev libgl-dev git cmake`

RedHat/CentOS/Fedora: `$ sudo yum install libXmu-devel libXi-devel libGL-devel git cmake`

##### Build

	$ cd build
	$ cmake ./cmake 
	$ make -j4

### Windows

Use the provided Visual Studio project file in build/vc12/

## glewinfo

`glewinfo` is a command-line tool useful for inspecting the capabilities of an
OpenGL implementation and GLEW support for that.  Please include the output of
`glewinfo` with bug reports, as appropriate.	

	---------------------------
	    GLEW Extension Info
	---------------------------

	GLEW version 2.0.0
	Reporting capabilities of pixelformat 3
	Running on a Intel(R) HD Graphics 3000 from Intel
	OpenGL version 3.1.0 - Build 9.17.10.4229 is supported

	GL_VERSION_1_1:                                                OK
	---------------

	GL_VERSION_1_2:                                                OK
	---------------
	  glCopyTexSubImage3D:                                         OK
	  glDrawRangeElements:                                         OK
	  glTexImage3D:                                                OK
	  glTexSubImage3D:                                             OK
	
	...

## Code Generation

A Unix or Mac environment is neded for building GLEW from scratch to
include new extensions, or customize the code generation. The extension
data is regenerated from the top level source directory with:

	make extensions

An alternative to generating the GLEW sources from scratch is to
download a pre-generated (unsupported) snapshot:

https://sourceforge.net/projects/glew/files/glew/snapshots/

Travis-built snapshots are also available:

https://glew.s3.amazonaws.com/index.html

## Authors

GLEW is currently maintained by [Nigel Stewart](https://github.com/nigels-com)
with bug fixes, new OpenGL extension support and new releases.

GLEW was developed by [Milan Ikits](http://www.cs.utah.edu/~ikits/)
and [Marcelo Magallon](http://wwwvis.informatik.uni-stuttgart.de/~magallon/).
Aaron Lefohn, Joe Kniss, and Chris Wyman were the first users and also
assisted with the design and debugging process.  

The acronym GLEW originates from Aaron Lefohn.
Pasi K&auml;rkk&auml;inen identified and fixed several problems with
GLX and SDL.  Nate Robins created the `wglinfo` utility, to
which modifications were made by Michael Wimmer.  

## Copyright and Licensing

GLEW is originally derived from the EXTGL project by Lev Povalahev.
The source code is licensed under the 
[Modified BSD License](http://glew.sourceforge.net/glew.txt), the 
[Mesa 3-D License](http://glew.sourceforge.net/mesa.txt) (MIT) and the
[Khronos License](http://glew.sourceforge.net/khronos.txt) (MIT).

The automatic code generation scripts are released under the 
[GNU GPL](http://glew.sourceforge.net/gpl.txt).
