cmake_minimum_required(VERSION 3.10)
project(formatter_ex_lib VERSION 1.0.0 LANGUAGES CXX)

set(SOURCES formatter_ex.cpp)
set(HEADERS formatter_ex.h)

add_library(formatter_ex STATIC ${SOURCES} ${HEADERS})

target_link_libraries(formatter_ex PRIVATE formatter)

target_include_directories(formatter_ex PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
target_include_directories(formatter_ex PRIVATE ${CMAKE_SOURCE_DIR}/formatter_lib)

set_target_properties(formatter_ex PROPERTIES
    ARCHIVE_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/lib
)
