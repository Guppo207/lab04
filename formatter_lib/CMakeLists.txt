cmake_minimum_required(VERSION 3.4)
project(formatter_lib LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED TRUE)

add_library(formatter_lib STATIC formatter.cpp)
