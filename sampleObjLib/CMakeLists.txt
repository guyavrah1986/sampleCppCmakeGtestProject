# CMakeLists.txt file for the sampleObj1 library

set(libName "sampleObj1Lib")

message(STATUS "CMakeLists.txt of ${libName} library")

add_library(${libName} sampleObj1.cxx)
