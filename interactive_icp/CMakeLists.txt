#project name
PROJECT(interactive_icp)

find_package(PCL 1.7 REQUIRED)
include_directories(${PCL_INCLUDE_DIRS})
link_directories(${PCL_LIBRARY_DIRS})
add_definitions(${PCL_DEFINITIONS})

message(STATUS "PCL_INCLUDE_DIRS:" ${PCL_INCLUDE_DIRS})
message(STATUS "PCL_LIBRARY_DIRS:" ${PCL_LIBRARY_DIRS})
message(STATUS "PCL_DEFINITIONS:" ${PCL_DEFINITIONS})

###########
## Build ##
###########
INCLUDE_DIRECTORIES(include)

add_executable(interactive_icp src/interactive_icp.cpp)
target_link_libraries(interactive_icp
  ${PCL_LIBRARIES}
)

