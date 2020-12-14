cmake_minimum_required(VERSION 2.8.3)
project(tocabi_controller)

## Compile as C++11, supported in ROS Kinetic and newer

## Find catkin macros and libraries
## if COMPONENTS list like find_package(catkin REQUIRED COMPONENTS xyz)
## is used, also find other catkin packages
find_package(catkin REQUIRED COMPONENTS
  geometry_msgs
  message_generation
  sensor_msgs
  std_msgs
)
add_message_files(
  FILES
  GainCommand.msg
  MotorInfo.msg
  TaskCommand.msg
  TaskCommandQue.msg
  TaskGainCommand.msg
  positionCommand.msg
  torqueCommand.msg
  model.msg
  VelocityCommand.msg
)
generate_messages(
  DEPENDENCIES
  geometry_msgs   sensor_msgs   std_msgs
)
catkin_package()
