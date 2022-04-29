set(module_name "app")

file(GLOB_RECURSE SRCS *.c)

# configure compiler
set(CMAKE_C_FLAGS "-g ${CMAKE_C_FLAGS}")
message(STATUS "modules c flags: " ${CMAKE_C_FLAGS})

add_executable(${module_name} ${SRCS})

# won't find file recursively
target_include_directories(${module_name} PUBLIC
  "${CMAKE_CURRENT_SOURCE_DIR}/include"
)

target_link_libraries(${module_name} PUBLIC m shared static)
#target_link_libraries(${module_name} PUBLIC m)
