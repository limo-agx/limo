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

if (CATKIN_ENABLE_TESTING)
  find_package(roslaunch REQUIRED)
  roslaunch_add_file_check(launch/limo_navigation_amcl_ackerman.launch)
  roslaunch_add_file_check(launch/limo_navigation_amcl_diff.launch)
  roslaunch_add_file_check(launch/limo_gmapping.launch)
  roslaunch_add_file_check(launch/limo_move_base_ackerman.launch)
  roslaunch_add_file_check(launch/limo_move_base_diff.launch)
  roslaunch_add_file_check(launch/limo_navigation_rtabmap_diff.launch)
  roslaunch_add_file_check(launch/limo_navigation_rtabmap_ackerman.launch)
  roslaunch_add_file_check(launch/limo_rtabmap.launch)
endif()
