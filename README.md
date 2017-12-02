# Boost-CMake

A simple CMake wrapper around the boost build. This repo can be included as a submodule into any project that requires the boost libraries.

This project can be used as follows:

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

You can then add the path to the boost headers to your include directories:

```cmake
include_directories(${Boost_INCLUDE_DIR})
```

And link against the boost libraries:

```cmake
target_link_libraries(${PROJECT_NAME} ${Boost_PROGRAM_OPTIONS_LIBRARY_DEBUG})
target_link_libraries(MyTest ${Boost_UNIT_TEST_FRAMEWORK_LIBRARY_RELEASE})
```
