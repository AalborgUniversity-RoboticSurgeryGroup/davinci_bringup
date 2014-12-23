cmake_minimum_required(VERSION 2.8.3)
project(davinci_bringup)

find_package(catkin REQUIRED)

catkin_package(
 CATKIN_DEPENDS rviz
)

install(FILES
  launch/visualization.launch
  launch/view_cameras.launch
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)
