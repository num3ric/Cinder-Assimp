Cinder-Assimp
-------------

C++ [Cinder](http://libcinder.org) Block to use the [Open Asset Import
Library](http://assimp.sourceforge.net/). Assimp is a portable Open Source
library to import various well-known 3D model formats in a uniform manner.

Based on [ofxAssimpModelLoader](https://github.com/openframeworks/openFrameworks/tree/master/addons/ofxAssimpModelLoader) by Anton Marini, Memo Akten, Kyle McDonald
and Arturo Castro.

###To do list

* VBO support, instead of TriMesh
* GPU skinning
* Better material support
* Multitexture support

###Static library rebuild instructions

The Cinder-Assimp block has a statically compiled version included.
The static library can be recompiled with the following steps:

Download Assimp from
http://sourceforge.net/projects/assimp/files/assimp-3.0/assimp--3.0.1270-source-only.zip/download

####Build instructions on OSX

<pre>
git clone git://github.com/assimp/assimp.git
cd assimp
cmake -G "Unix Makefiles" -DBOOST_ROOT="../cinder_master/boost" -DCMAKE_CXX_FLAGS="-stdlib=libc++ -fvisibility-inlines-hidden" -DCMAKE_BUILD_TYPE=Release -DASSIMP_BUILD_STATIC_LIB=true -DCMAKE_OSX_ARCHITECTURES="i386;x86_64"
make
</pre>

which creates libassimp.a in the lib/ directory.

####Build instructions on Windows

...

