cmake_minimum_required(VERSION 3.16.3)
project(hello_world)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_executable(hello_world hello_world.cpp)

include_directories(~/Laba3/hello_world_application/../formatter_ex_lib)
target_link_libraries(hello_world formatter_ex)
