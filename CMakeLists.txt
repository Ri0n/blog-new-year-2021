cmake_minimum_required(VERSION 3.17)
project(rhhpl_project VERSION 1.0.0 DESCRIPTION "Richard Hodges's HTTP pool library")

option(BUILD_TOOLS "Build example tools" ON)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_MODULE_PATH "${CMAKE_MODULE_PATH}" "${CMAKE_CURRENT_SOURCE_DIR}/cmake/modules")

add_subdirectory(src)
if (BUILD_TOOLS)
    add_subdirectory(tools)
endif()
