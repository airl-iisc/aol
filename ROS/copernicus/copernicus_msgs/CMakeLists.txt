cmake_minimum_required(VERSION 2.8.3)
project(copernicus_msgs)

find_package(catkin REQUIRED COMPONENTS
  message_generation
  std_msgs
)

add_message_files(
  DIRECTORY msg
  FILES
  Velocities.msg
  BMS.msg
  RPM.msg
  Diagnostics.msg
  SonarSensor.msg
)

generate_messages(DEPENDENCIES std_msgs)

catkin_package(
  CATKIN_DEPENDS
  std_msgs
  message_runtime
)