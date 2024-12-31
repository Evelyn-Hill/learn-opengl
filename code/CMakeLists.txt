cmake_minimum_required(VERSION 3.0.0)
project(learnopengl VERSION 0.1.0)
cmake_policy(SET CMP0072 NEW)

find_package(OpenGL REQUIRED)

add_executable(learn_opengl 
  src/main.cpp
  src/glad.h
  src/glad.c
)

target_link_libraries(learn_opengl 
  glfw
  OpenGL::GL
)
