cmake_minimum_required(VERSION 3.10)
project(solver LANGUAGES CXX)

add_executable(solve
    equation.cpp
)

target_include_directories(hello_world
    PRIVATE
    ${CMAKE_CURRENT_SOURCE_DIR}/../formatter_ex_lib
)

target_link_libraries(solve
    PRIVATE
    formatter_ex
    solver_lib
)
