#cmake version
cmake_minimum_required(VERSION 3.0)

#Project information
project("ZWHH-DFS")

#build agrc
set(CMAKE_CXX_FLAGS_RELEASE "$ENV{CXXFLAGS} -O3 -Wall -std=c++17")

add_definitions(-std=c++17)

#executable output path
set(EXECUTABLE_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/bin)

#head filse path
set(INC_LIST ${CMAKE_SOURCE_DIR}/include)

#include head files
include_directories(${INC_LIST})

#add cmake subdirectory
add_subdirectory(src)

#add executable files
add_executable(ZWHH-DFS ${PROJECT_SOURCE_DIR}/main.cpp)

#add link
target_link_libraries(ZWHH-DFS source-objects)
