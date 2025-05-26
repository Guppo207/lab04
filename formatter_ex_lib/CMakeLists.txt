cmake_minimum_required(VERSION 3.10)

project(
    formatter_ex
    VERSION 1.0.0
    DESCRIPTION "Extended formatter library"
    LANGUAGES CXX
)


add_library(formatter_ex STATIC
    formatter_ex.cpp
    formatter_ex.h
)


target_include_directories(formatter_ex
    PUBLIC
    $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}>
    $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/../formatter_lib>
    $<INSTALL_INTERFACE:include>
)


set_target_properties(formatter_ex PROPERTIES
    CXX_STANDARD 17
    CXX_STANDARD_REQUIRED ON
    CXX_EXTENSIONS OFF
)

find_package(formatter REQUIRED)
target_link_libraries(formatter_ex
    PUBLIC
    formatter
)


install(
    TARGETS formatter_ex
    ARCHIVE DESTINATION lib
    LIBRARY DESTINATION lib
    PUBLIC_HEADER DESTINATION include
)


export(
    TARGETS formatter_ex
    FILE "${CMAKE_CURRENT_BINARY_DIR}/formatter_exConfig.cmake"
)
