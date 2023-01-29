cmake_minimum_required(VERSION 3.25)

project(leetcode)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_C_COMPILER "/usr/bin/clang")
set(CMAKE_CXX_COMPILER "/usr/bin/clang++")
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

add_executable(leetcode main.cc)
target_link_options(leetcode PRIVATE -fsanitize=address,leak,undefined -fno-omit-frame-pointer)
target_compile_options(leetcode PRIVATE -fsanitize=address,leak,undefined -fno-omit-frame-pointer)
