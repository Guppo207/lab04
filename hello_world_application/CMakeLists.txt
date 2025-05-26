cmake_minimum_required(VERSION 3.4)

project(
    hello_world
    VERSION 1.0
    DESCRIPTION "Hello World Application"
    LANGUAGES CXX
)


set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

add_subdirectory(../formatter_ex_lib formatter_ex_lib)


add_executable(hello_world hello_world.cpp)


target_include_directories(hello_world
    PUBLIC
    ../formatter_ex_lib
)


target_link_libraries(hello_world
    PRIVATE
    formatter_ex_lib
)
