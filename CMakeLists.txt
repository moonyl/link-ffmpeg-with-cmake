cmake_minimum_required(VERSION 3.15)
project(temporary)

set(CMAKE_CXX_STANDARD 14)

configure_file(CMakeLists.txt.in ffmpeg-download/CMakeLists.txt)
execute_process(COMMAND ${CMAKE_COMMAND} . WORKING_DIRECTORY ${CMAKE_CURRENT_BINARY_DIR}/ffmpeg-download)
execute_process(COMMAND ${CMAKE_COMMAND} --build . WORKING_DIRECTORY ${CMAKE_CURRENT_BINARY_DIR}/ffmpeg-download)

add_executable(temporary main.cpp)