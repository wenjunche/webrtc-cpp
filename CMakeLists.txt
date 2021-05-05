cmake_minimum_required(VERSION 3.20)

project(webrtc-cpp CXX)

add_executable(webrtc-cpp src/main.cpp)

find_package(fmt REQUIRED)

target_link_libraries(webrtc-cpp fmt)
