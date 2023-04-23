project(${CMAKE_PROJECT_NAME})

add_executable(triangle triangle.cpp)

target_link_libraries(triangle
  PRIVATE glfw
  PRIVATE glad)
