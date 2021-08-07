# https://www.glfw.org/docs/latest/build_guide.html#build_link_cmake_package
cmake_minimum_required(VERSION 3.13.4)

project(tamachan)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

find_package(OpenGL REQUIRED)
find_package(glfw3 3.3 REQUIRED)

add_executable(tamachan tamachan.cpp)
target_link_libraries(tamachan glfw OpenGL::GL)
