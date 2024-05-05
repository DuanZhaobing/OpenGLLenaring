cmake_minimum_required(VERSION 3.22)
project(HelloWindow)

set(CMAKE_CXX_STANDARD 11)
find_package(glfw3 REQUIRED)
file(GLOB project_file glad.c main.cpp)
add_executable(${PROJECT_NAME} ${project_file}
        src/glad.c)
target_link_libraries(${PROJECT_NAME} glfw)
