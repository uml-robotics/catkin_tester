cmake_minimum_required(VERSION 2.8.3)
project(std_capabilities)

find_package(catkin REQUIRED)

catkin_package()

install(DIRECTORY interfaces
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION})
