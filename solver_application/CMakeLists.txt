cmake_minimum_required(VERSION 3.10)
project(solver VERSION 1.0.0 LANGUAGES CXX)

add_executable(solver equation.cpp)

target_link_libraries(solver PRIVATE formatter_ex solver_lib)

target_include_directories(solver PRIVATE
    ${CMAKE_SOURCE_DIR}/formatter_ex_lib
    ${CMAKE_SOURCE_DIR}/formatter_lib
    ${CMAKE_SOURCE_DIR}/solver_lib
)
