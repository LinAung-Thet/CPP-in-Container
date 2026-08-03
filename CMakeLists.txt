cmake_minimum_required(VERSION 3.16)

project(leetcode_app LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Set the CMAKE_EXPORT_COMPILE_COMMANDS variable to ON to generate a compile_commands.json file 
#that lists every compiler command used to build the project.
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

# Do not compile targets with position‑independent code (PIC): 
# having PIC enabled can cause issues with certain libraries or when linking with certain flags.
set(CMAKE_POSITION_INDEPENDENT_CODE OFF)

# Build the executable as a non‑PIE (non–position‑independent executable).
set(CMAKE_EXE_LINKER_FLAGS "${CMAKE_EXE_LINKER_FLAGS} -no-pie")

# Add the src folder so that CMake Tools can see targets inside it
add_subdirectory(src)

add_executable(mincoin src/MinCoinsForFruits.cpp)