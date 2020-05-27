cmake_minimum_required(VERSION 3.10)

project(Zenova)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED True)

add_subdirectory("${PROJECT_SOURCE_DIR}/Common")
add_subdirectory("${PROJECT_SOURCE_DIR}/ZenovaLoader")
add_subdirectory("${PROJECT_SOURCE_DIR}/ZenovaAPI")