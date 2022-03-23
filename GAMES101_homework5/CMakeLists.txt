cmake_minimum_required(VERSION 3.15)
project(GAMES101_homework5)

set(CMAKE_CXX_STANDARD 17)

add_executable(GAMES101_homework5 main.cpp Object.hpp Vector.hpp Sphere.hpp global.hpp Triangle.hpp Scene.cpp Scene.hpp Light.hpp Renderer.cpp)