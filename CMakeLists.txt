
cmake_minimum_required(VERSION 3.10)
project(FMP4ProcessingServer)
set(CMAKE_CXX_STANDARD 17)

find_package(OpenCV REQUIRED)
find_package(FFMPEG REQUIRED)

include_directories(
    ${OpenCV_INCLUDE_DIRS}
    ${FFMPEG_INCLUDE_DIRS}
)

add_executable(server main.cpp)

target_link_libraries(server
    ${OpenCV_LIBS}
    ${FFMPEG_LIBRARIES}
)
