cmake_minimum_required(VERSION 3.0.2)
project(r2d2_msg_pkg)

add_compile_options(-std=c++17)

find_package(catkin REQUIRED COMPONENTS
  std_msgs
  message_generation
)

################################################
## Declare ROS messages, services and actions ##
################################################

## Generate messages in the 'msg' folder
add_message_files(
   FILES
   DriverState.msg
   DriverCommand.msg
   PipeParameters.msg
 )

## Generate services in the 'srv' folder
add_service_files(
  FILES
  GetParams.srv
  ManipulatorCommand.srv
)

## Generate added messages and services with any dependencies listed above
generate_messages(
  DEPENDENCIES
  std_msgs
)

###################################
## catkin specific configuration ##
###################################

catkin_package(
  CATKIN_DEPENDS std_msgs
)
