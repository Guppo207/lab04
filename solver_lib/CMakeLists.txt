cmake_minimum_required(VERSION 3.4)

project(
    solver_lib
    VERSION 1.0
    LANGUAGES CXX
    DESCRIPTION "Library for mathematical solving"
)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

add_library(solver_lib
    ${CMAKE_CURRENT_SOURCE_DIR}/solver.cpp
)
