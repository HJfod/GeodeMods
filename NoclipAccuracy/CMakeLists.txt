cmake_minimum_required(VERSION 3.3.0)
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

project(RunInfo VERSION 1.0.0)

# Use GLOB_RECURSE instead of GLOB
# to recursively add all source files 
# under src/ 
file(GLOB SOURCES
	src/*.cpp
)

# Set up the mod binary
add_library(${PROJECT_NAME} SHARED ${SOURCES})
set_target_properties(${PROJECT_NAME} PROPERTIES PREFIX "")

target_link_libraries(${PROJECT_NAME} geode-sdk)
create_geode_file(${PROJECT_NAME})
