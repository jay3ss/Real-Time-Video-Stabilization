cmake_minimum_required(VERSION 2.8)
project(RealTimeVideoStabilization)
include_directories(include)
find_package(OpenCV REQUIRED)

# add sources manually
set(SOURCES src/main.cpp src/videostab.cpp)

# file(GLOB...) allows for wildcard addition of sources
#file(GLOB "src/*.cpp")

add_executable(main ${SOURCES})
target_link_libraries(main ${OpenCV_LIBS})
