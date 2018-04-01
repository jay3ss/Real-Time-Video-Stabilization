cmake_minimum_required(VERSION 2.8)
project(RealTimeVideoStabilization)

if(UNIX)
    SET(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wall -std=gnu++0x")
endif()

include_directories(include)
find_package(OpenCV REQUIRED)

# add sources manually
set(MAIN_SOURCES src/main.cpp src/videostab.cpp)
set(STABILIZE_VIDEO_SOURCES 
    src/stabilize_video.cpp 
    src/videostab.cpp)
set(KALMAN_VIDEO_SOURCES src/video_stab_kalman.cpp)

# file(GLOB...) allows for wildcard addition of sources
# file(GLOB "src/*.cpp")

add_executable(main ${MAIN_SOURCES})
target_link_libraries(main ${OpenCV_LIBS})

add_executable(stabilize_video ${STABILIZE_VIDEO_SOURCES})
target_link_libraries(stabilize_video ${OpenCV_LIBS})

add_executable(video_stab_kalman ${KALMAN_VIDEO_SOURCES})
target_link_libraries(video_stab_kalman ${OpenCV_LIBS})
