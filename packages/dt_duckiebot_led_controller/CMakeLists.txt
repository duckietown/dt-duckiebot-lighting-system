cmake_minimum_required(VERSION 2.8.3)
project(dt_duckiebot_led_controller)

find_package(catkin REQUIRED COMPONENTS
  duckietown_msgs
  rospy
  message_generation
  std_msgs
)


## Generate services in the 'srv' folder
add_service_files(
  FILES
  SetCustomLEDColors.srv
)

add_message_files(
  FILES
  LEDColor.msg
  LEDColorArray.msg
)

generate_messages(
  DEPENDENCIES
  std_msgs
)


catkin_package()


include_directories(
  ${catkin_INCLUDE_DIRS}
)
