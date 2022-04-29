set(lib_name "shared")

file(GLOB_RECURSE SRCS *.c)

# configure compiler
message(STATUS "lib shared flags: " ${CMAKE_C_FLAGS})

add_library(${lib_name} SHARED ${SRCS})

target_include_directories(${lib_name} PUBLIC
  "${CMAKE_CURRENT_SOURCE_DIR}/include"
)
