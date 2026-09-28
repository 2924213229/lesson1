cmake_minimum_required(VERSION 3.16)
project(lesson1 LANGUAGES CXX)

add_executable(hello main.cpp)

set_target_properties(hello PROPERTIES
    CXX_STANDARD 17
    CXX_STANDARD_REQUIRED ON
    CXX_EXTENSIONS OFF
)

target_compile_options(hello PRIVATE -Wall -g)
