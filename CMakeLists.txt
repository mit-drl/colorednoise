cmake_minimum_required(VERSION 2.8.3)
project(colorednoise)

set(CMAKE_CXX_FLAGS "-std=c++11 ${CMAKE_CXX_FLAGS}")
set(CMAKE_CXX_FLAGS "-Wno-write-strings -g ${CMAKE_CXX_FLAGS}")

find_package(catkin_simple REQUIRED)

catkin_python_setup()

catkin_simple(ALL_DEPS_REQUIRED)

cs_install()

cs_export()

if (CATKIN_ENABLE_TESTING)
  find_package(rostest REQUIRED)
endif()
