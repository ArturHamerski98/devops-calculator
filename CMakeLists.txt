cmake_minimum_required(VERSION 3.16)

project(Calculator LANGUAGES CXX)

add_library(CalcHeader STATIC main.cpp calculator.hpp)
add_library(CalcTest STATIC test.cpp calculator.hpp)
add_executable(Calculator main.cpp)
add_executable(Test test.cpp)


target_link_libraries(Calculator CalcHeader)
target_link_libraries(Test CalcTest)

