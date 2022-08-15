# Top level cmake for individual subprojects
cmake_minimum_required(VERSION 3.24)

# Adding internal projects to compilation
add_subdirectory(library)
add_subdirectory(executable)

# Adding external dependencies as subprojects
#add_subdirectory(external/)

# Adding include directories to project executable
target_include_directories(CPP_Executable PUBLIC library/src)

# Adding link directories to project executable
target_link_directories(CPP_Executable PRIVATE library)

# Linking libraries to project executable
target_link_libraries(CPP_Executable CPP_Library)