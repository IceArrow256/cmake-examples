cmake_minimum_required(VERSION 3.20)

project(app VERSION 1.0)

add_subdirectory(extern/lib)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED True)

add_executable(app)

target_sources(app PRIVATE 
              ${CMAKE_CURRENT_SOURCE_DIR}/src/main.cpp
              ${CMAKE_CURRENT_SOURCE_DIR}/src/app.cpp
	      )

target_include_directories(app PRIVATE
                          ${CMAKE_CURRENT_SOURCE_DIR}/include
			  )

target_link_libraries(app PUBLIC lib)

