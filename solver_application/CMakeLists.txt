cmake_minimum_required(VERSION 3.4)

project(
    solver
    VERSION 1.0
    DESCRIPTION "Equation solver application"
    LANGUAGES CXX
)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

add_subdirectory(../formatter_ex_lib formatter_ex_lib)
add_subdirectory(../solver_lib solver_lib)


add_executable(solver equation.cpp)

target_include_directories(solver
    PUBLIC
    ../formatter_ex_lib
    ../solver_lib
)


target_link_libraries(solver
    PRIVATE
    formatter_ex_lib
    solver_lib
)
