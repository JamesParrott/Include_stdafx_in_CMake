# Include stdafx.h in CMake
A way to avoid deleting the first line (`#include stdafx.h`) of every file in the entire code base when porting Visual Studio projects to CMake, using a compiler definition and a little C++ templating. 

## To compile:
* `cmake -B build -S .`
* `cmake --build build`