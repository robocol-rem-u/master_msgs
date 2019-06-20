cmake_minimum_required(VERSION 2.8.3)
project(master_msgs)

find_package(catkin REQUIRED COMPONENTS
  geometry_msgs
  message_generation
)

add_message_files(
  FILES
  arm_Orders.msg
  connection.msg
  current.msg
  goal.msg
  imu_Magnetism.msg
  imu_Speed.msg
  position.msg
  pots.msg
  rpm.msg
  traction_Orders.msg
  sensibility.msg
)

)

#add_service_files(
 # FILES
  #AckService.srv
  #EndService.srv
  #StartService.srv
#)

generate_messages(
  DEPENDENCIES 
  geometry_msgs
)

catkin_package(
   CATKIN_DEPENDS geometry_msgs message_runtime
)
