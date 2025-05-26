cmake_minimum_required(VERSION 3.15)
project(FFmpeg LANGUAGES C)

add_library(FFmpeg STATIC dummy.c)  

file(GLOB_RECURSE LIBRARIES "${CMAKE_CURRENT_SOURCE_DIR}/*.lib")
target_link_libraries(FFmpeg PUBLIC ${LIBRARIES})

target_include_directories(FFmpeg PUBLIC "${CMAKE_CURRENT_SOURCE_DIR}/include")
