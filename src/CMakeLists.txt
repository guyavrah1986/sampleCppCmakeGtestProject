# CMakeLists.txt file for the main application (executable)

set(exeName "mainApplication")

message(STATUS "CMakeLists.txt of ${exeName} executable")


# add the sampleObj1Lib library
add_subdirectory(sampleObj1Lib)

# add the executable
add_executable(${exeName} main.cxx)

target_link_libraries(${exeName} PUBLIC sampleObj1Lib)

# add the binary tree to the search path for include files
# so that we will find sampleObj1.h
target_include_directories(${exeName} PUBLIC
                          "${PROJECT_BINARY_DIR}"
                          "${PROJECT_SOURCE_DIR}/sampleObj1Lib"
                          )
