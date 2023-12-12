cmake_minimum_required(VERSION 3.27)
project(WaterSurfaceProject)

set(CMAKE_CXX_STANDARD 17)
set(OpenGlLinkers -lglfw -lGL -ldl -lGLEW -lassimp)
add_executable(WaterSurfaceProject main.cpp
        Shader.h
        stb_image.h
        stbimg.cpp
        Camera.h
        Mesh.h
        Model.h
)
find_package(OpenGL REQUIRED)
include_directories(${OPENGL_INCLUDE_DIRS})
target_link_libraries(WaterSurfaceProject  ${OpenGlLinkers})

