cmake_minimum_required(VERSION 3.28)
project(Raycaster)

set(CMAKE_CXX_STANDARD 11)

set(GLFW_ROOT "${CMAKE_SOURCE_DIR}/libs/glfw-3.4")

include_directories(${GLFW_ROOT}/include)

link_directories(${GLFW_ROOT}/lib-mingw-w64)

add_executable(Raycaster main.cpp)

find_package(OpenGL REQUIRED)
target_link_libraries(Raycaster ${OPENGL_LIBRARIES} glfw3 -lOpenGL32 -lfreeGLUT)