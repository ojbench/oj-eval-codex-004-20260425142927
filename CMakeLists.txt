cmake_minimum_required(VERSION 3.10)
project(bookstore_oj_004 LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

add_executable(code
    src/main.cpp
)

if (MSVC)
  target_compile_options(code PRIVATE /W4 /permissive-)
else()
  target_compile_options(code PRIVATE -Wall -Wextra -Wpedantic -O2)
endif()

