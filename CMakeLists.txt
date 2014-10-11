#
# @file CMakeLists.txt
# @author Akagi201
# @date 2014/10/10
#

cmake_minimum_required(VERSION 2.8.4)
project(ffmpeg_muxer)

set(SOURCE_FILES main.c)

include_directories("/usr/local/include")

link_directories("/usr/local/lib")

add_executable(ffmpeg_muxer ${SOURCE_FILES})

target_link_libraries(ffmpeg_muxer "libavformat.a")

target_link_libraries(ffmpeg_muxer "libavcodec.a")

target_link_libraries(ffmpeg_muxer "libavutil.a")