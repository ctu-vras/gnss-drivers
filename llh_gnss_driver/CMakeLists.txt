cmake_minimum_required(VERSION 3.8.2)
project(llh_gnss_driver)

find_package(catkin REQUIRED COMPONENTS message_generation sensor_msgs std_msgs)

add_message_files(FILES
  LlhFix.msg
  NavSatDetailedStatus.msg
  NavSatFixQuality.msg
)

generate_messages(DEPENDENCIES
  sensor_msgs
  std_msgs
)

catkin_package(CATKIN_DEPENDS
  message_runtime
  sensor_msgs
  std_msgs
)
