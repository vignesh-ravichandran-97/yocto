cmake_minimum_required(VERSION 3.13)

project(CMakeTest)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wall")
set(EXECUTABLE_OUTPUT_PATH ${CMAKE_BINARY_DIR}/bin)


add_executable(sample_app appsrc/sample_app.c)
add_subdirectory(lib)
target_include_directories(sample_app PUBLIC "${CMAKE_SOURCE_DIR}/include")
target_link_libraries(sample_app sample)
