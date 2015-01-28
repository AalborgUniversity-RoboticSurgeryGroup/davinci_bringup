cmake_minimum_required(VERSION 2.8.3)
project(davinci_bringup)

find_package(catkin REQUIRED)

catkin_package(
 CATKIN_DEPENDS rviz davinci_driver davinci_moveit_config
 DEPENDS v4l-utils
)

install(PROGRAMS
  scripts/camera_v4l2_settings.bash
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)

install(FILES
  launch/cameras.launch
  launch/visualization.launch
  launch/view_cameras.launch
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)
