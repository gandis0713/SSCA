cmake_minimum_required(VERSION 3.12)

# The information about project.
project(
triangle
VERSION 0.1
DESCRIPTION "Triangle sample"
LANGUAGES CXX
)

add_executable(triangle main.cpp)

target_include_directories(
  ${PROJECT_NAME}
  PUBLIC
	${Vulkan_INCLUDE_DIRS}
)

target_link_libraries(${PROJECT_NAME}
  PRIVATE
	${Vulkan_LIBRARIES}
  glfw
)

# target_compile_options(triangle PUBLIC -Wall -Werror -fno-rtti)