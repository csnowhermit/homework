cmake_minimum_required(VERSION 3.15)
project(GAMES101_homework3)

set(CMAKE_CXX_STANDARD 17)

include_directories(C:/workspace/opt/include)

# 设置OpenCV目录所在
set(CMAKE_MODULE_PATH "C:/workspace/gitrepo/OpenCV-MinGW-Build-OpenCV-4.5.5-x64")    # Module模式，在指定目录下只查找FindXXX.cmake文件。如果没找到该文件，cmake进入config模式
set(OpenCV_DIR "C:/workspace/gitrepo/OpenCV-MinGW-Build-OpenCV-4.5.5-x64")    # Config模式，在指定目录下只查找xxxConfig.cmake文件。

# 搜索OpenCV目录
find_package(OpenCV REQUIRED)

# 添加OpenCV头文件目录
#include_directories(${OpenCV_INCLUDE_DIRS})
include_directories(C:/workspace/gitrepo/OpenCV-MinGW-Build-OpenCV-4.5.5-x64/include)
link_directories(C:/workspace/gitrepo/OpenCV-MinGW-Build-OpenCV-4.5.5-x64/x64/mingw/lib)


add_executable(GAMES101_homework3 main.cpp rasterizer.hpp rasterizer.cpp global.hpp Triangle.hpp Triangle.cpp Texture.hpp Texture.cpp Shader.hpp OBJ_Loader.h)

target_link_libraries(GAMES101_homework3  ${OpenCV_LIBS})