cmake_minimum_required(VERSION 3.10)
project(solver_lib VERSION 1.0.0 LANGUAGES CXX)

set(SOURCES solver.cpp)
set(HEADERS solver.h)

add_library(solver_lib STATIC ${SOURCES} ${HEADERS})

target_include_directories(solver_lib PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})

set_target_properties(solver_lib PROPERTIES
    ARCHIVE_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/lib
)
