cmake_minimum_required(VERSION 3.16)

set(pname "base-cmake")
project(${pname})

# set static library output path
set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY ${PROJECT_BINARY_DIR}/lib)
# set dynamic library output path
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${PROJECT_BINARY_DIR}/bin)
# set execute file output path
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${PROJECT_BINARY_DIR}/bin)

set(CMAKE_C_COMPILER gcc)
set(CMAKE_CXX_COMPILER g++)
set(CMAKE_C_FLAGS "-std=c99 -o0 ${CMAKE_C_FLAGS}")
set(CMAKE_CXX_FLAGS "-o0 ${CMAKE_CXX_FLAGS}")
add_compile_options(-Wall -fPIC)

# build dynamic lib
add_subdirectory(lib_shared)
# include_directories(lib_shared)

# build static lib
add_subdirectory(lib_static)
# include_directories(lib_static)

# build modules
add_subdirectory(modules)

# configure
add_subdirectory(configure)
