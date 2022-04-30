cmake_minimum_required(VERSION 3.0)
project(qp)


set(CMAKE_CXX_FLAGS "-std=c++11")
link_directories("/usr/local/lib")
include_directories("/usr/local/include")
aux_source_directory(. SRC_LIST) # 搜索当前目录下的所有.cpp文件
add_executable(qp ${SRC_LIST})
target_link_libraries(qp libqpOASES.so)

