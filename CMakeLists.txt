cmake_minimum_required(VERSION 2.8)

project(VXLHelpers)

include_directories(${CMAKE_CURRENT_SOURCE_DIR})

FIND_PACKAGE(VXL REQUIRED)
INCLUDE(${VXL_CMAKE_DIR}/UseVXL.cmake)

set(libVXL vnl vnl_algo vcl vil vbl vgl vgl_algo vul)

add_library(VXLHelpers VXLHelpers.cpp)
target_link_libraries(VXLHelpers libVXL)
