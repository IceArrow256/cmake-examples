cmake_minimum_required(VERSION 3.10)

project(lib VERSION 1.0)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED True)

add_library(lib)

target_sources(lib PRIVATE
              ${CMAKE_CURRENT_SOURCE_DIR}/src/hello.cpp
              )

target_include_directories(lib PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/include)
