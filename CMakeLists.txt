cmake_minimum_required(VERSION 3.0)
project(learnopengl)

set (INCLUDE_DIRS
    ./external/glad/include
    ${INCLUDE_DIRS}
)

include_directories(${INCLUDE_DIRS})

# Compile external dependencies
add_subdirectory (external)
add_subdirectory (playground)
add_subdirectory (2.1.hello_triangle)
