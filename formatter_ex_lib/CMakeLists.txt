cmake_minimum_required(VERSION 3.5)
project(formatter_ex LANGUAGES CXX)

add_library(formatter_ex STATIC formatter_ex.cpp)
target_link_libraries(formatter_ex PUBLIC formatter)
target_include_directories(formatter_ex PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
