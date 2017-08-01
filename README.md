# Using OpenCV in Visual Studio
1. Configuration Properties > VC++ Directories
  * for Include Directories option, provide built opencv include directory paths that contain all the header files
  * for Library Directories option, provide Release and Debug directory paths that contain .dll's (opencv_world320.dll, opencv_world320d.dll)
    * Would suggest using $(SolutionDir) and $(Configuration) variables.
    * example: $(SolutionDir)/$(Configuration)
2. Configuration Properties > Linker > Input
  * for Additional Include Dependencies, use opencv_ts320.lib and opencv_world320.lib for Release Configuration, and opencv_ts320d.lib and opencv_world320d.lib for Debug Configuration
  * not sure if Linker > General > Link Library Dependencies need to be yes, it seems to work either way (idk).
