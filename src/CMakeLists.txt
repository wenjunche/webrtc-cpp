cmake_minimum_required(VERSION 3.20)

add_executable(webrtc-cpp main.cpp)

option(CMAKE_USE_WIN32_THREADS_INIT "using WIN32 threads" ON)

find_package(fmt CONFIG REQUIRED)
find_package(cxxopts CONFIG REQUIRED)
find_package(Libdatachannel CONFIG REQUIRED)

target_link_libraries(webrtc-cpp 
    PRIVATE 
        fmt::fmt
        cxxopts::cxxopts
        LibDatachannel::datachannel
    )
