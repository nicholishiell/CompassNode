cmake_minimum_required(VERSION 2.8.3)
project(compass_node)

find_package(catkin REQUIRED COMPONENTS std_msgs roscpp)

include_directories(${catkin_INCLUDE_DIRS})
set(EXECUTABLE_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/bin)
set(LIBRARY_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/lib)

add_executable(
  compass_node 
  src/compass_node.cpp 
)	 

target_link_libraries(compass_node ${catkin_LIBRARIES})

