file(GLOB_RECURSE MAIN_FILES CONFIGURE_DEPENDS
  ${CMAKE_CURRENT_SOURCE_DIR}/main.cpp
)

add_executable(program ${MAIN_FILES})
target_link_libraries(program PUBLIC ffmpeg)