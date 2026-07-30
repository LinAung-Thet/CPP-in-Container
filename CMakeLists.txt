cmake_minimum_required(VERSION 3.16)

project(leetcode_app LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_executable(myapp
    src/MinCoinsForFruits.cpp
)

# Cross-platform warning flags
if (MSVC)
    target_compile_options(myapp PRIVATE /W4)
else()
    target_compile_options(myapp PRIVATE -Wall -Wextra -Wpedantic)
endif()