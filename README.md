# Boost-CMake

A simple CMake wrapper around the boost build. This repo can be included as a submodule into any project that requires the boost libraries.

This can be used as follows:

```cmake
set(BOOST_REQUIRED_COMPONENTS test program_options)
add_subdirectory(boost-cmake)
find_package(
  Boost
  1.64.0
  COMPONENTS
  program_options
  unit_test_framework
)
```
