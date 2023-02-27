add_executable(ffmpeg ${MAIN_FILES})

target_link_libraries(ffmpeg ${FFMPEG_LIBS})
target_include_directories(ffempg
  PUBLIC
    ${CMAKE_CURRENT_SOURCE_DIR}/build/include/libavcodec
    ${CMAKE_CURRENT_SOURCE_DIR}/build/include/libavdevice
    ${CMAKE_CURRENT_SOURCE_DIR}/build/include/libavfilter
    ${CMAKE_CURRENT_SOURCE_DIR}/build/include/libavformat
    ${CMAKE_CURRENT_SOURCE_DIR}/build/include/libavutil
    ${CMAKE_CURRENT_SOURCE_DIR}/build/include/libswscale
)