cmake_minimum_required(VERSION 2.8)
project( PCN )
set(CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} /home/mattia/Scrivania/opencv/build)
if(UNIX)
    SET(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wall -std=gnu++0x")
endif()
find_package( OpenCV REQUIRED )
include_directories( ${OpenCV_INCLUDE_DIRS} )
add_executable( PCN main.cpp )
target_link_libraries( PCN ${OpenCV_LIBS} )
