cmake_minimum_required(VERSION 3.10)
project(formatter LANGUAGES CXX)

add_library(formatter STATIC 
    formatter.cpp
    formatter.h
)
