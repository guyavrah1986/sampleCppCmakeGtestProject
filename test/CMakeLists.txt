# CMakeLists.txt for the unit tests:
# =================================

message(STATUS "unit tests CMakeLists.txt of ${CMAKE_PROJECT_NAME}")
 
# Locate GTest
find_package(GTest REQUIRED)
include_directories(${GTEST_INCLUDE_DIRS})
 
# Link runTests with what we want to test and the GTest and pthread library
find_library(GTEST_LIBRARY gtest HINTS /usr/lib)
message(STATUS "GTEST_INCLUDE_DIRS is: ${GTEST_INCLUDE_DIRS}")
message(STATUS "GTEST_LIBRARY is: ${GTEST_LIBRARY}")
message(STATUS "GTEST_LIBRARIES is: ${GTEST_LIBRARIES}")

add_executable(unitTestsExe main.cpp) # SampleObj1-test.cpp
target_link_libraries(unitTestsExe ${GTEST_LIBRARY} pthread)
