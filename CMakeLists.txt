cmake_minimum_required(VERSION 3.12)

# Project name
project(DIP_HW05)

# Find OpenCV package and include it
find_package( OpenCV REQUIRED )
include_directories( ${OpenCV_INCLUDE_DIRS} )

# Set C++ 11
set( CMAKE_CXX_STANDARD 11 )
set( CMAKE_CXX_STANDARD_REQUIRED ON )
set( CMAKE_CXX_EXTENSIONS OFF )

# Project sources
set( SOURCE_DIR src )
set( PROJECT_SOURCES
        ${SOURCE_DIR}/common.h
        ${SOURCE_DIR}/common.cpp
)

# The main program
add_executable( DIP_HW05 ${SOURCE_DIR}/main.cpp ${PROJECT_SOURCES} )

# Add link libraries
target_link_libraries( DIP_HW05 ${OpenCV_LIBS} )