cmake_minimum_required(VERSION 2.8.3)
project(ros_images_publisher)

find_package(catkin REQUIRED COMPONENTS
  roscpp
  rospy
  std_msgs
  sensor_msgs
  geometry_msgs
)

install(
  FILES publish_images.py
  PERMISSIONS OWNER_EXECUTE GROUP_EXECUTE WORLD_EXECUTE
  DESTINATION /ros/install/share/ros_images_publisher
)

catkin_package(CATKIN_DEPENDS message_runtime) # declares dependencies for packages that depend on this package.

include_directories(
  ${catkin_INCLUDE_DIRS}
)
