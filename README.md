# Using OpenCV in Visual Studio
1. Configuration Properties > VC++ Directories
  * for Include Directories option, provide path to _built_ opencv directories containing all the header files
    * Note: you should probably include the parent directory of the "opencv" and "opencv2" so that when you include header files in source files, it's ```#include <opencv2\core.hpp>``` instead of just ```#include <core.hpp>```.
  * for Library Directories option, provide Release and Debug directory paths that contain the library/object files (opencv_world320.dll, opencv_world320d.dll, opencv_world320.lib, opencv_world320d.lib, etc.).
    * Would suggest using $(SolutionDir) and $(Configuration) variables.
    * example: $(SolutionDir)/$(Configuration)
2. Configuration Properties > Linker > Input
  * for Additional Include Dependencies, use opencv_world320.lib for Release Configuration, and opencv_world320d.lib for Debug Configuration.
  * not sure if Linker > General > Link Library Dependencies need to be yes, it seems to work either way (idk).
