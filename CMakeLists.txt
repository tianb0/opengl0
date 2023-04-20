cmake_minimum_required(VERSION 3.23)

project(hello)

set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

add_executable(main main.cpp)

add_subdirectory(external/glfw)
add_subdirectory(external/glad)

target_include_directories(main PUBLIC external/glfw/include)

target_link_directories(main PRIVATE external/glfw/src)

target_link_libraries(main
  PRIVATE glfw
  PRIVATE glad)
