
cmake_minimum_required(VERSION 3.4.1)

aux_source_directory(. DIR_JNI_SOURCE)
include_directories(./ ./lzma1805/C)
add_subdirectory(./lzma1805/C)

add_library(native-lib SHARED ${DIR_JNI_SOURCE})

target_link_libraries(native-lib log lzma1805)