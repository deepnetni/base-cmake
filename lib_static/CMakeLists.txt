set(lib_name "static")

file(GLOB_RECURSE SRCS *.c)

# configure compiler
add_compile_options(-g)
message(STATUS "lib static flags: " ${CMAKE_C_FLAGS})

add_library(${lib_name} STATIC ${SRCS})

target_include_directories(${lib_name} PUBLIC
  "${CMAKE_CURRENT_SOURCE_DIR}/include"
)
