cmake_minimum_required(VERSION 2.8)

project(podcastgen)

set(CMAKE_C_FLAGS "-O3 -std=gnu99")

add_executable(podcastgen src/main.c src/util.c src/sound.c src/files.c)
target_link_libraries(podcastgen sndfile)

install(TARGETS podcastgen DESTINATION bin)
