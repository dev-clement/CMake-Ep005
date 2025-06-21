cmake_minimum_required(VERSION 3.15)
project(HelloApp
        VERSION 0.0.1
        DESCRIPTION "The leading hello world app"
        LANGUAGES CXX)


# Using globbing
# Although, globbing is a technic that is discouraged by all the CMake community
file(GLOB_RECURSE SOURCE_FILES src/*.cpp)
add_executable(HelloAppBinary main.cpp ${SOURCE_FILES})

# Target
# add_executable(HelloAppBinary main.cpp src/dog.cpp src/operations.cpp)

target_compile_features(HelloAppBinary PRIVATE cxx_std_20)
target_include_directories(HelloAppBinary PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/include)