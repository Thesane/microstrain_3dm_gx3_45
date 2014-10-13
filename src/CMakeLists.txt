cmake_minimum_required(VERSION 2.8.3)
project(microstrain_3dm_gx3_45)

## Find catkin macros and libraries
## if COMPONENTS list like find_package(catkin REQUIRED COMPONENTS xyz)
## is used, also find other catkin packages
find_package(catkin REQUIRED COMPONENTS
  roscpp
  std_msgs
)

## System dependencies are found with CMake's conventions
# find_package(Boost REQUIRED COMPONENTS system)


## Uncomment this if the package has a setup.py. This macro ensures
## modules and global scripts declared therein get installed
## See http://ros.org/doc/api/catkin/html/user_guide/setup_dot_py.html
# catkin_python_setup()

################################################
## Declare ROS messages, services and actions ##
################################################

## To declare and build messages, services or actions from within this
## package, follow these steps:
## * Let MSG_DEP_SET be the set of packages whose message types you use in
##   your messages/services/actions (e.g. std_msgs, actionlib_msgs, ...).
## * In the file package.xml:
##   * add a build_depend and a run_depend tag for each package in MSG_DEP_SET
##   * If MSG_DEP_SET isn't empty the following dependencies might have been
##     pulled in transitively but can be declared for certainty nonetheless:
##     * add a build_depend tag for "message_generation"
##     * add a run_depend tag for "message_runtime"
## * In this file (CMakeLists.txt):
##   * add "message_generation" and every package in MSG_DEP_SET to
##     find_package(catkin REQUIRED COMPONENTS ...)
##   * add "message_runtime" and every package in MSG_DEP_SET to
##     catkin_package(CATKIN_DEPENDS ...)
##   * uncomment the add_*_files sections below as needed
##     and list every .msg/.srv/.action file to be processed
##   * uncomment the generate_messages entry below
##   * add every package in MSG_DEP_SET to generate_messages(DEPENDENCIES ...)

## Generate messages in the 'msg' folder
# add_message_files(
#   FILES
#   Message1.msg
#   Message2.msg
# )

## Generate services in the 'srv' folder
# add_service_files(
#   FILES
#   Service1.srv
#   Service2.srv
# )

## Generate actions in the 'action' folder
# add_action_files(
#   FILES
#   Action1.action
#   Action2.action
# )

## Generate added messages and services with any dependencies listed here
# generate_messages(
#   DEPENDENCIES
#   std_msgs
# )

###################################
## catkin specific configuration ##
###################################
## The catkin_package macro generates cmake config files for your package
## Declare things to be passed to dependent projects
## INCLUDE_DIRS: uncomment this if you package contains header files
## LIBRARIES: libraries you create in this project that dependent projects also need
## CATKIN_DEPENDS: catkin_packages dependent projects also need
## DEPENDS: system dependencies of this project that dependent projects also need
catkin_package(
#  INCLUDE_DIRS include
#  LIBRARIES microstrain_3dm_gx3_45
#  CATKIN_DEPENDS roscpp std_msgs
#  DEPENDS system_lib
)

###########
## Build ##
###########

## Specify additional locations of header files
## Your package locations should be listed before other locations
# include_directories(include)
include_directories(
  ${catkin_INCLUDE_DIRS}
  
)

## Declare a cpp library
#add_library(mip_sdk_user_functions
#   Include/mip_sdk_user_functions.cpp Include/mip_sdk_user_functions.h Include/mip.h Include/mip_types.h 
#)
#add_library(byteswap_utilities
#   Include/byteswap_utilities.cpp Include/byteswap_utilities.h Include/mip_types.h
#)

#add_library(mip_sdk_system
#   Include/mip_sdk_system.cpp Include/mip_sdk_system.h Include/mip.h Include/mip_types.h Include/mip_sdk_interface.h Include/mip_sdk_config.h Include/mip_sdk_user_functions.h Include/mip.h Include/ring_buffer.h Include/byteswap_utilities.h Include/mip_types.h
#)
#add_library(mip_sdk_base
#   Include/mip_sdk_base.cpp  Include/mip_sdk_base.h Include/mip.h Include/mip_types.h Include/mip_sdk_interface.h Include/mip_sdk_config.h Include/mip_sdk_user_functions.h Include/mip.h Include/ring_buffer.h Include/byteswap_utilities.h Include/mip_types.h
#)
#add_library(mip_sdk_gps
#   Include/mip_sdk_gps.cpp Include/mip_sdk_gps.h Include/mip.h Include/mip_types.h Include/mip_sdk_interface.h Include/mip_sdk_config.h Include/mip_sdk_user_functions.h Include/mip.h Include/ring_buffer.h Include/byteswap_utilities.h Include/mip_types.h
#)
#add_library(mip
#   Include/mip.cpp Include/mip.h Include/mip_types.h
#)
#add_library(mip_sdk_3dm
#   Include/mip_sdk_3dm.cpp Include/mip_sdk_3dm.h Include/mip.h Include/mip_types.h Include/mip_sdk_interface.h Include/mip_sdk_config.h Include/mip_sdk_user_functions.h Include/mip.h Include/ring_buffer.h Include/byteswap_utilities.h Include/mip_types.h Include/mip_sdk_gps.h Include/mip_sdk_ahrs.h
#)
#add_library(ring_buffer
#   Include/ring_buffer.cpp Include/ring_buffer.h Include/mip_types.h
#)
#add_library(mip_sdk_inteface
#   Include/mip_sdk_inteface.cpp Include/mip_sdk_interface.h Include/mip.h Include/mip_types.h Include/mip_sdk_config.h Include/mip_sdk_user_functions.h Include/mip.h Include/ring_buffer.h Include/byteswap_utilities.h Include/mip_types.h
#)
#add_library(mip_sdk_filter
#   Include/mip_sdk_filter.cpp Include/mip_sdk_filter.h Include/mip.h Include/mip_types.h Include/mip_sdk_interface.h Include/mip_sdk_config.h Include/mip_sdk_user_functions.h Include/mip.h Include/ring_buffer.h Include/byteswap_utilities.h Include/mip_types.h Include/mip_sdk_system.h
#)

#add_library(mip_sdk_ahrs
#   Include/mip_sdk_ahrs.cpp Include/mip_sdk_ahrs.h Include/mip.h Include/mip_types.h Include/mip_sdk_interface.h Include/mip_sdk_config.h Include/mip_sdk_user_functions.h Include/mip.h Include/ring_buffer.h Include/byteswap_utilities.h Include/mip_types.h 
#)






## Declare a cpp executable
add_executable(GX3_45 driver.cpp driver.h node.h node.cpp )

## Add cmake target dependencies of the executable/library
## as an example, message headers may need to be generated before nodes
#add_dependencies(GX3_45 mip_sdk_system mip_sdk_base mip_sdk_gps mip mip_sdk_3dm ring_buffer mip_sdk_inteface mip_sdk_filter mip_sdk_ahrs mip_sdk_user_functions byteswap_utilities )

## Specify libraries to link a library or executable target against
target_link_libraries(GX3_45
   ${catkin_LIBRARIES} 
)

#############
## Install ##
#############

# all install targets should use catkin DESTINATION variables
# See http://ros.org/doc/api/catkin/html/adv_user_guide/variables.html

## Mark executable scripts (Python etc.) for installation
## in contrast to setup.py, you can choose the destination
install(PROGRAMS
#   scripts/my_python_script
   DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)

## Mark executables and/or libraries for installation
install(TARGETS GX3_45
   ARCHIVE DESTINATION ${CATKIN_PACKAGE_LIB_DESTINATION}
   LIBRARY DESTINATION ${CATKIN_PACKAGE_LIB_DESTINATION}
   RUNTIME DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
 )

## Mark cpp header files for installation
# install(DIRECTORY include/${PROJECT_NAME}/
#   DESTINATION ${CATKIN_PACKAGE_INCLUDE_DESTINATION}
#   FILES_MATCHING PATTERN "*.h"
#   PATTERN ".svn" EXCLUDE
# )

## Mark other files for installation (e.g. launch and bag files, etc.)
# install(FILES
#   # myfile1
#   # myfile2
#   DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
# )

#############
## Testing ##
#############

## Add gtest based cpp test target and link libraries
# catkin_add_gtest(${PROJECT_NAME}-test test/test_microstrain_3dm_gx3_45.cpp)
# if(TARGET ${PROJECT_NAME}-test)
#   target_link_libraries(${PROJECT_NAME}-test ${PROJECT_NAME})
# endif()

## Add folders to be run by python nosetests
# catkin_add_nosetests(test)
