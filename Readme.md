# TurboFetch

Copy-pasta for all your CMake needs.

Using `find_package` to add dependencies to a CMake project requires the user to either have the library installed or to build it manually beforehand. This means that the user has to manually deal with the projects dependencies, which can be annoying if they just quickly want to clone and compile some random project.

At some point CMake added `ExternalProject_Add` which can download and build dependencies at configure time, but this doesn't allow for the same flexibility as the newer `FetchContent` module.

It can however sometimes be a bit cumbersome to get the FetchContent usage right, especially with differing conventions in various projects, this is where this snippet copy-paste resource steps in.

Add this to your CMakeLists.txt

```cmake
include(FetchContent)

# paste some TurboFetch snippets here, adjust `_TAG_` and `_TARGET_` placeholders
```

Most of the snippets require CMake 3.14 or above, this should not be a problem anymore nowadays, not even for Ubuntu LTS.
