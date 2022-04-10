# 指定工程名称
project(EmbedCTK)

include_directories( ${CMAKE_SOURCE_DIR}/HelloCTK)


add_executable(EmbedCTK main.cpp)
target_link_libraries(EmbedCTK 
  HelloCTK
)

