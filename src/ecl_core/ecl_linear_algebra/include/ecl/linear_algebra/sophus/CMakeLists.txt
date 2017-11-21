###############################################################################
# Files
###############################################################################

message("dir3:=${CMAKE_SOURCE_DIR}/sophus")
include_directories(${CMAKE_SOURCE_DIR}/sophus)

file(GLOB HEADERS RELATIVE ${CMAKE_CURRENT_SOURCE_DIR} *.hpp)

install(FILES ${HEADERS} DESTINATION include/ecl/linear_algebra/sophus)
