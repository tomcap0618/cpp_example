# example
# example
# Copyright 2020, Thomas Capuano
cmake_minimum_required(VERSION 3.1)
project(example C CXX)
set(PROJECT_DESCRIPTION   "example")
set(PROJECT_AUTHOR        "Thomas Capuano")
set(PROJECT_URL           "https://github.com/tcapuano/example")
set(PROJECT_VERSION_MAJOR "0")
set(PROJECT_VERSION_MINOR "0")
set(PROJECT_VERSION_PATCH "1")

# Build flags
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -O3 -march=native")
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wall -Wextra -Werror -pedantic")


# ---------------------------------------------------------
# Features
# ---------------------------------------------------------
add_subdirectory(external)
add_subdirectory(src)

enable_testing()
add_subdirectory(test)
add_subdirectory(doc)
