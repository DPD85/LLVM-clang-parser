# LLVM-clang-parser
LLVM + clang v3.8.0 already configured for a minimal build of clang parser for people that need only the clang parser

## How to build
### On Unix-like Systems
1. Get the required tools:
  * See [Getting Started with the LLVM System - Requirements](http://llvm.org/docs/GettingStarted.html#requirements) for details on requirements for build LLVM. Following the most important tools:
    * **GNU Make**	3.79 or 3.79.1
    * **GCC** 4.7.0 or later
  * **CMake**. This is used for generating the make files. Get it from: http://www.cmake.org/cmake/resources/software.html
  * **Python 2.7**. This is needed only if you will be running the tests (which is essential, if you will be developing for clang). Get it from: http://www.python.org/download/
2. Clone this repository inside llvm folder
3. Run CMake to generate the make files:
  * Go 1 folder outside of llvm directory
  * mkdir build
  * cd build
  * cmake -G "Unix Makefiles" ../llvm
4. Build clang
  * Inside the build folder run: make

### Using Visual Studio
1. Get the required tools:
  * **CMake**. This is used for generating Visual Studio solution and project files. Get it from: http://www.cmake.org/cmake/resources/software.html
  * **Visual Studio 2013** or later
  * **Python 2.7**. This is needed only if you will be running the tests (which is essential, if you will be developing for clang). Get it from: http://www.python.org/download/
2. Clone this repository
3. Run CMake to generate the Visual Studio solution and project files:
  * Create a 'build' directory outside of the reposotiry (for building without polluting the source dir)
  * Open cmake-gui
  * For source code folder specify the repository directory
  * For folder where to build the binaries specify the 'build' directory
  * Presso the 'Generate' button and select the version of Visual Studio you want to use for build (2013 or later)
  * See the [LLVM CMake guide](http://www.llvm.org/docs/CMake.html) for more information on other configuration options for CMake.
  * The above, if successful, will have created an LLVM.sln file in the 'build' directory.
4. Build clang:
  * Open LLVM.sln in Visual Studio.
  * Build the "clang" project for just the compiler driver and front end, or the "ALL_BUILD" project to build everything, including tools.

## See also
* clang get started guide: http://clang.llvm.org/get_started.html
* Some example of program using the clang parser:
  * PrivateDeclarationRemover: https://bitbucket.org/dpd/privatedeclarationremover
  * clang_indexer: https://github.com/exclipy/clang_indexer
  * clang-extract: https://github.com/sk-havok/clang-extract
  * include-what-you-use: https://github.com/include-what-you-use/include-what-you-use
  
