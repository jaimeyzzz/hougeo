cmake_minimum_required(VERSION 2.8)
project( "hougeo" )

include_directories( ${CMAKE_CURRENT_SOURCE_DIR} )

IF ( NOT WIN32 )
  ADD_DEFINITIONS ( -fPIC )
ENDIF ()

IF (APPLE)
  ADD_DEFINITIONS ( -std=c++11 )
ENDIF ()

# hougeo library ---
add_subdirectory( hougeo )

# test and demo applications ---
add_subdirectory( tests )
