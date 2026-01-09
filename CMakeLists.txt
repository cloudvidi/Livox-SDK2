cmake_minimum_required(VERSION 3.10)

project(livox_sdk2)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)


get_property(is_multi_config GLOBAL PROPERTY GENERATOR_IS_MULTI_CONFIG)
if(NOT is_multi_config AND NOT CMAKE_BUILD_TYPE)
  set(CMAKE_BUILD_TYPE "Release" CACHE STRING "Choose the type of build, options are: Debug Release RelWithDebInfo MinSizeRel." FORCE)
  message(STATUS "Default build type set to Release")
endif()


find_package(Threads REQUIRED)

message(STATUS "main project dir: " ${PROJECT_SOURCE_DIR})

add_subdirectory(sdk_core)
add_subdirectory(samples)
