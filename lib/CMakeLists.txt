cmake_minimum_required(VERSION 3.13)

project(lib)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wall")
set(EXECUTABLE_OUTPUT_PATH ${CMAKE_BINARY_DIR}/lib)

set (LIB_SOURCES add.c sub.c)
add_library (sample SHARED ${LIB_SOURCES})

target_include_directories(sample PUBLIC "${CMAKE_SOURCE_DIR}/include/shared")
