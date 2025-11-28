# min version of cmake
cmake_minimum_required(VERSION 3.10)

# name of project
project(LibrarySystem VERSION 1.0)

file(GLOB SOURCE_FILES "src/*.cpp")

add_executable(LibrarySystem ${SOURCE_FILES})
target_include_directories(LibrarySystem PUBLIC include)

