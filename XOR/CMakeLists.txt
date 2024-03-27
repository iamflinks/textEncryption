cmake_minimum_required(VERSION 3.0...3.25)
project(
    CPOINTTER C # name of the project, which will also be the name of the visual studio solution if you use it
    VERSION 0.1.0 # any version number
    LANGUAGES CXX C # programming languages used by the project
)


add_executable(xorEncryption xorEncryption.c)

set_target_properties(xorEncryption PROPERTIES
    CXX_STANDARD 17
    CXX_EXTENSIONS OFF
    COMPILE_WARNING_AS_ERROR ON
)

set(CMAKE_DEBUG_POSTFIX "d")


# Steps to build a C++ program using CMake

# cmake . -B build -G "MinGW Makefiles"
# cmake --build build
# build\Debug\App.exe  # Windows (Not working on VScode because there is no debug folder)
# build/App  # this works