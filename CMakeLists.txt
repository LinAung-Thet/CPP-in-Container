cmake_minimum_required(VERSION 3.16)

project(leetcode_app LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Always use a separate build directory
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

set(CMAKE_POSITION_INDEPENDENT_CODE OFF)
set(CMAKE_EXE_LINKER_FLAGS "${CMAKE_EXE_LINKER_FLAGS} -no-pie")

# Add the src folder so CMake Tools can see targets inside it
add_subdirectory(src)

add_executable(mincoin src/MinCoinsForFruits.cpp)