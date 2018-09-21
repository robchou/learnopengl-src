cmake_minimum_required(VERSION 3.0)
project(glad)

include_directories(include)
set(GLAD_SOURCE src/glad.c)

add_library(glad STATIC ${GLAD_SOURCE})
