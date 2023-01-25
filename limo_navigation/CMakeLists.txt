cmake_minimum_required(VERSION 3.0.2)
project(limo_navigation)

find_package(catkin REQUIRED COMPONENTS)

catkin_package(
#  INCLUDE_DIRS include
#  LIBRARIES limo_navigation
#  CATKIN_DEPENDS gmapping map_server move_base
#  DEPENDS system_lib
)

include_directories(
# include
  ${catkin_INCLUDE_DIRS}
)
