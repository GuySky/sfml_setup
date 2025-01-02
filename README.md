# SFML setup
   
This repository is the basic setup to start working with Super Fast Media Library version 2.6.1. It was built with GCC 14.2.0 on Windows 10 and will work the best on the same set.
After building there will be dynamic libraries in the same folder with .exe-file. These libraries (dll) are known to be easier to be utilized by newbies.
If you want your project to be based on static libraries, you'll have to download and compile all the required dependencies for SFML before building. If you use Windows 10 or higher, you'll probably already have the most of required libs, except for FreeType and Jpeg. Good luck building them)
   
To start working with SFML, all you need is to clone this rep to your machine and build it with cmake. Just use these commands in any terminal:

```
cd *PATH_TO_YOUR_PROJECT*
cmake -S . -B build -G "MinGW Makefiles"
cd build
mingw32-make
```
"MinGW Makefiles" should be changed to whatever generator you use, which depends on your compiler. Also to make it with mingw32-make you have to have [MinGW](https://sourceforge.net/projects/mingw/) installed and [set up the environment variables](https://semicolon.dev/windows/how-to-install-mingw-gcc-g-compiler-windows-10-11-2023). Same thing with [Cmake](https://cmake.org/download/).

### So the literal guide for Windows 10+

1. [Install git](https://git-scm.com/downloads/win).
2. [Install Cmake](https://cmake.org/download/).
3. Install [MinGW](https://sourceforge.net/projects/mingw/files/Installer/) or [MSYS2 (recommended)](https://www.msys2.org).
4. Set the environment variables[1](https://semicolon.dev/windows/how-to-install-mingw-gcc-g-compiler-windows-10-11-2023)[2](https://www.freecodecamp.org/news/how-to-install-c-and-cpp-compiler-on-windows/).
5. [Clone](https://git-scm.com/docs/git-clone) this repository to your machine. For example, in "C:/dev/SFML_projects/".
6. Open terminal (Win+R, type cmd).
7. Go to your directory (cd C:/dev/SFML_projects).
8. `cmake -S . -B build -G "MinGW Makefiles"`
9. `cd build`
10. `mingw32-make`

Now you have your .exe-file in build/ directory as well as all the needed .dll-libs. If by executing the program you get an error like "missing entry point" or sth, that means you have a different version of compiler from what the dlls were built with. In that case you'll need to build the SFML sources yourself, but it's easy, you'll figure it out.

if you need any help, you can upload an Issue to this rep on github, or just contact me.