cmake_minimum_required(VERSION 3.15)
project(Algorithms)

enable_testing()
set(CMAKE_COMPILE_WARNING_AS_ERROR ON)
if (MSVC)
    # needs at least cmake 3.15
    add_compile_options(/W2 /WX /wd4100)
else()
    add_compile_options(-Wall -Wextra -Wpedantic -Wno-gnu-empty-struct -Wno-unused-parameter)
endif()

add_subdirectory(LibraryCPP)
add_subdirectory(LibraryCPPClass)
add_subdirectory(LibraryCPPTemplate)

add_subdirectory(Lab2CPPTemplate)
