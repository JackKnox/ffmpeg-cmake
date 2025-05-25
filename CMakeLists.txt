cmake_minimum_required(VERSION 3.15)
project(FFmpeg LANGUAGES C)

file(GLOB LIBRARIES "lib/**.lib")

target_link_libraries(FFmpeg PUBLIC ${LIBRARIES})
target_include_directories(FFmpeg PUBLIC "${STRYPE_LIBRARIES}/include")