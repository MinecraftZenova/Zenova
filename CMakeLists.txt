cmake_minimum_required(VERSION 3.10)

project(Zenova)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED True)

include_directories("${PROJECT_SOURCE_DIR}/Common")
add_subdirectory("${PROJECT_SOURCE_DIR}/Common")
add_subdirectory("${PROJECT_SOURCE_DIR}/ZenovaAPI")

if(MSVC)
    foreach(OUTPUTCONFIG ${CMAKE_CONFIGURATION_TYPES})
        string(TOUPPER ${OUTPUTCONFIG} OUTPUTCONFIG)
        set(CMAKE_RUNTIME_OUTPUT_DIRECTORY_${OUTPUTCONFIG} "${PROJECT_SOURCE_DIR}/Zenova/Bin/")
        set(CMAKE_LIBRARY_OUTPUT_DIRECTORY_${OUTPUTCONFIG} "${PROJECT_SOURCE_DIR}/Zenova/Bin/")
        set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY_${OUTPUTCONFIG} "${PROJECT_SOURCE_DIR}/Zenova/Bin/")
    endforeach(OUTPUTCONFIG CMAKE_CONFIGURATION_TYPES)
endif()

add_subdirectory("${PROJECT_SOURCE_DIR}/ZenovaGUI")
add_subdirectory("${PROJECT_SOURCE_DIR}/ZenovaLoader")