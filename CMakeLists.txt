cmake_minimum_required(VERSION 3.0)
set(CMAKE_CXX_COMPILER "D:/environment/minggw64/mingw64/bin/g++.exe")
set(CMAKE_C_COMPILER "D:/environment/minggw64/mingw64/bin/gcc.exe")
project(windows_cmake_gl)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wall")

set(CMAKE_BUILD_TYPE Debug)
aux_source_directory(src SRC_CUR)
aux_source_directory(. SRC_CUR)
include_directories(${CMAKE_SOURCE_DIR}/include)
# 设置可执行文件输出目录为output
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_SOURCE_DIR}/output)


add_executable(my_cmake_exe ${SRC_SUB} ${SRC_CUR})
#target_link_libraries(my_cmake_exe ${CMAKE_SOURCE_DIR}/lib/libglfw3dll.a ${CMAKE_SOURCE_DIR}/lib/libglad.a)
target_link_libraries(my_cmake_exe  ${CMAKE_SOURCE_DIR}/lib/libglfw3.a ${CMAKE_SOURCE_DIR}/lib/libglfw3dll.a  ${CMAKE_SOURCE_DIR}/lib/libglad.a)


