cmake_minimum_required(VERSION 3.16)

project(cmake_test_1)

add_library(cmake_test_1
        source/cmake_test_1/Utils.h
        source/cmake_test_1/Utils.cpp)

target_include_directories(cmake_test_1 PUBLIC source)

set_target_properties(cmake_test_1
        PROPERTIES
        ARCHIVE_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/lib"
        LIBRARY_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/lib"
        RUNTIME_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/bin"
        )