cmake_minimum_required(VERSION 3.14)
project(example_cmake_ctest LANGUAGES C)

if (BUILD_TESTING)
  include(CTest)
  enable_testing()

  add_subdirectory(tests)
endif()
