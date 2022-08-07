cmake_minimum_required(VERSION 3.10)

# set the project name
project(openGLDonut VERSION 1.0)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED True)

find_package(glfw3 3.3 REQUIRED)

# Add .lib files
link_directories(${CMAKE_SOURCE_DIR}/Libraries/lib ${CMAKE_DL_LIBS})
include_directories(${CMAKE_SOURCE_DIR}/Libraries/include)

# Add source files
file(GLOB_RECURSE SOURCE_FILES 
${CMAKE_SOURCE_DIR}/*.c
${CMAKE_SOURCE_DIR}/*.cpp)

# Add header files
file(GLOB_RECURSE HEADER_FILES 
${CMAKE_SOURCE_DIR}/*.h
${CMAKE_SOURCE_DIR}/*.hpp)

# add the executable# Define the executable
add_executable(${PROJECT_NAME} ${HEADER_FILES} ${SOURCE_FILES})
