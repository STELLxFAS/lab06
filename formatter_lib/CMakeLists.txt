cmake_minimum_required(VERSION 3.10)
project(formatter_lib VERSION 1.0.0 LANGUAGES CXX)

set(SOURCES formatter.cpp)
set(HEADERS formatter.h)

add_library(formatter STATIC ${SOURCES} ${HEADERS})

target_include_directories(formatter PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})

set_target_properties(formatter PROPERTIES
    ARCHIVE_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/lib
)
