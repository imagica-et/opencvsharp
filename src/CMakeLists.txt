cmake_minimum_required(VERSION 3.10)

project(OpenCvSharpExtern)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")

# Avoid installing to /usr/local by default; user can override with -DCMAKE_INSTALL_PREFIX=...
if(CMAKE_INSTALL_PREFIX_INITIALIZED_TO_DEFAULT)
	set(CMAKE_INSTALL_PREFIX "${CMAKE_SOURCE_DIR}/install" CACHE PATH "Default install prefix" FORCE)
endif()

#set(CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} "${CMAKE_SOURCE_DIR}/cmake/Modules/")

# remove MinSizeRel & RelWithDebInfo
SET(CMAKE_CONFIGURATION_TYPES "Debug;Release" CACHE STRING "limited configs" FORCE)

add_subdirectory(OpenCvSharpExtern) 
