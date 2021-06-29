cmake_minimum_required(VERSION 3.20)

project(app VERSION 1.0)

add_subdirectory(extern/lib)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED True)

add_executable(app main.cpp)

target_link_libraries(app PUBLIC lib)

