cmake_minimum_required(VERSION 3.15)
project(temporary)

set(CMAKE_CXX_STANDARD 14)
include(ExternalProject)
ExternalProject_Add(ffmpeg
        URL https://ffmpeg.zeranoe.com/builds/win64/dev/ffmpeg-4.2.2-win64-dev.zip
        CONFIGURE_COMMAND ""
        BUILD_COMMAND ""
        INSTALL_COMMAND ""
        #INSTALL_COMMAND ${CMAKE_COMMAND} -E echo ${CMAKE_CURRENT_BINARY_DIR}/ffmpeg-prefix ${CMAKE_SOURCE_DIR}
        )

add_executable(temporary main.cpp)