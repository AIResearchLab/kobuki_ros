cmake_minimum_required(VERSION 3.8)
project(kobuki_gazebo)

if(CMAKE_COMPILER_IS_GNUCXX OR CMAKE_CXX_COMPILER_ID MATCHES "Clang")
  add_compile_options(-Wall -Wextra -Wpedantic)
endif()

find_package(ament_cmake REQUIRED)
find_package(urdf REQUIRED)
find_package(xacro REQUIRED)

install(DIRECTORY launch DESTINATION share/${PROJECT_NAME})

ament_export_dependencies(${dependencies})

ament_package()