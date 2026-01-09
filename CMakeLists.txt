cmake_minimum_required(VERSION 3.10)

project(livox_sdk2)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

find_package(Threads REQUIRED)

message(STATUS "main project dir: " ${PROJECT_SOURCE_DIR})

add_subdirectory(sdk_core)
add_subdirectory(samples)
