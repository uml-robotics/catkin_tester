###############################################################################
# Test Macro
###############################################################################

macro(ecl_sigslots_add_gtest test_name)
  catkin_add_gtest(ecl_test_${test_name} ${test_name}.cpp)
  if(TARGET ecl_test_${test_name})
    target_link_libraries(ecl_test_${test_name} ${catkin_LIBRARIES})
  endif()
endmacro()

###############################################################################
# Google Tests
###############################################################################

ecl_sigslots_add_gtest(sigslots sigslots.cpp)
