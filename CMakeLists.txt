cmake_minimum_required(VERSION 3.4)


project(
    cmake_project_suite
    VERSION 1.0.0
    DESCRIPTION "Collection of CMake projects"
    LANGUAGES CXX
)


set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)


foreach(component 
    formatter_lib
    formatter_ex_lib
    hello_world_application
    solver_lib
    solver_application
)
    add_subdirectory(${component})
endforeach()
