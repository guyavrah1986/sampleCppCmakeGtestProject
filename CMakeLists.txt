#This is the project's main CMakeLists.txt
#======================================== 

cmake_minimum_required(VERSION 3.5)

project(sampleProject)

message(STATUS "main CMakeLists.txt of ${CMAKE_PROJECT_NAME}")

set(CMAKE_CXX_STANDARD 14)
set (CMAKE_CXX_FLAGS "-m32")
set (CMAKE_C_FLAGS "-m32")

include_directories(src)

add_subdirectory(src)

add_subdirectory(sampleObj1Lib)

add_subdirectory(test)

