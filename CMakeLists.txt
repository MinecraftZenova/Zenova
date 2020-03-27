cmake_minimum_required(VERSION 3.10)

project(Zenova)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED True)

if(DEFINED CMAKE_GENERATOR_PLATFORM)
    message(AUTHOR_WARNING "Platform: ${CMAKE_GENERATOR_PLATFORM}")
else()
    message(AUTHOR_WARNING "Platform: $ENV{CMAKE_GENERATOR_PLATFORM}")
endif()

add_subdirectory("${PROJECT_SOURCE_DIR}/Common")
include_directories("${PROJECT_SOURCE_DIR}/Common")

add_subdirectory("${PROJECT_SOURCE_DIR}/ZenovaAPI")
add_subdirectory("${PROJECT_SOURCE_DIR}/ZenovaGUI")
add_subdirectory("${PROJECT_SOURCE_DIR}/ZenovaLoader")