cmake_minimum_required(VERSION 3.4)
project(lab03)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

include_directories("../formatter_lib")
include_directories("../formatter_ex_lib")
include_directories("../solver_lib")
add_library(formatter_lib STATIC "../formatter_lib/formatter.cpp")
add_library(formatter_ex_lib STATIC "../formatter_ex_lib/formatter_ex.cpp")
add_library(solver_lib STATIC "../solver_lib/solver.cpp")

add_executable(lab03 "equation.cpp")
target_link_libraries(lab03 solver_lib formatter_ex_lib formatter_lib)