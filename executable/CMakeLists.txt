# CMake file for executable subproject
cmake_minimum_required(VERSION 3.24)
project(CPP_Executable)

# Required C++ standard (recomended 20)
set(CMAKE_CXX_STANDARD_REQUIRED 20)

# Setting up spurce directory and files for compilation
set(srcDir "${PROJECT_SOURCE_DIR}/src")
file(GLOB_RECURSE srcFiles "${srcDir}/*.cpp")

# Creating executable file
add_executable(${PROJECT_NAME} ${srcFiles})