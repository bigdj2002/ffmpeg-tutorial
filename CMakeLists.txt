cmake_minimum_required(VERSION 3.10)

project(
  ffmpeg-tutorial
  DESCRIPTION "Study ffmpeg"
  LANGUAGES CXX)

set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/lib)
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/lib)
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin)
set(FFMPEG_LIBS
  ${CMAKE_SOURCE_DIR}/libs/ffmpeg-5.1.2/build/lib/libavcodec.so.59.37.100
  ${CMAKE_SOURCE_DIR}/libs/ffmpeg-5.1.2/build/lib/libavdevice.so.59.7.100
  ${CMAKE_SOURCE_DIR}/libs/ffmpeg-5.1.2/build/lib/libavfilter.so.8.44.100		
  ${CMAKE_SOURCE_DIR}/libs/ffmpeg-5.1.2/build/lib/libavformat.so.59.27.100
  ${CMAKE_SOURCE_DIR}/libs/ffmpeg-5.1.2/build/lib/libavutil.so.57.28.100
  ${CMAKE_SOURCE_DIR}/libs/ffmpeg-5.1.2/build/lib/libswscale.so.6.7.100
)

add_subdirectory(libs)
add_subdirectory(src)