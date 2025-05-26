cmake_minimum_required(VERSION 3.4)

project(
    formatter_ex_lib
    VERSION 1.0
    LANGUAGES CXX
)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED TRUE)

get_filename_component(FORMATTER_LIB_DIR "../formatter_lib" ABSOLUTE)

add_subdirectory(${FORMATTER_LIB_DIR} formatter_lib_build)

add_library(formatter_ex_lib STATIC formatter_ex.cpp)

target_include_directories(
    formatter_ex_lib
    PUBLIC 
    ${FORMATTER_LIB_DIR}
)

target_link_libraries(
    formatter_ex_lib
    PRIVATE 
    formatter_lib
)
