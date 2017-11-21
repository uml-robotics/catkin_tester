###############################################################################
# SUBDIRECTORIES
###############################################################################

add_subdirectory(eigen)
add_subdirectory(sophus)
#include_directories(include ${catkin_INCLUDE_DIRS} ${sophus_INCLUDE_DIRS} ${CMAKE_SOURCE_DIR}/sophus/sophus)
#include_directories(${CMAKE_SOURCE_DIR}/sophus)
message("dir2:=${CMAKE_SOURCE_DIR}/sophus")
include_directories(${CMAKE_SOURCE_DIR}/sophus)

###############################################################################
# FILES
###############################################################################

file(GLOB HEADERS RELATIVE ${CMAKE_CURRENT_SOURCE_DIR} *.hpp)
  
install(FILES ${HEADERS} DESTINATION ${CATKIN_GLOBAL_INCLUDE_DESTINATION}/ecl/linear_algebra)

