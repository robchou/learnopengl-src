cmake_minimum_required(VERSION 3.0)
project(playground)
set(TARGET playground)

set (INCLUDE_DIRS
    ${INCLUDE_DIRS}
)

include_directories(${INCLUDE_DIRS})

find_package(OpenGL REQUIRED)
find_library(GLFW_LIBRARY glfw)
set(GLAD_LIBRARY glad)

if(UNIX)
    set (INCLUDE_DIRS
        "/usr/include"
        "/usr/local/include"
        "/usr/include/GL"
        ${INCLUDE_DIRS}
    )
endif(UNIX)

set(PROJECT_SOURCE playground.cpp)
add_executable(${TARGET} ${PROJECT_SOURCE})
target_link_libraries (${TARGET} ${OPENGL_LIBRARIES} ${GLFW_LIBRARY} ${GLAD_LIBRARY})
