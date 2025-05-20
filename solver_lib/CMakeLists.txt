cmake_minimum_required(VERSION 3.5)
project(solver_lib)

# Создаем статическую библиотеку
add_library(solver_lib STATIC solver.cpp)

# Подключаем зависимости
target_link_libraries(solver_lib PRIVATE formatter_ex)

# Указываем пути к заголовочным файлам
target_include_directories(solver_lib PUBLIC
    ${CMAKE_CURRENT_SOURCE_DIR}
    ${CMAKE_SOURCE_DIR}/formatter_ex_lib
    ${CMAKE_SOURCE_DIR}/formatter_lib
)
