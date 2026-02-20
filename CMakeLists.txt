cmake_minimum_required(VERSION 4.2.3)

project(CppKoans)

add_definitions(
  -std=c++0x -g -O0
)

set(cppkoans_SOURCES
  ${PROJECT_SOURCE_DIR}/cppkoans.cpp
  ${PROJECT_SOURCE_DIR}/helper.hpp
  ${PROJECT_SOURCE_DIR}/headers/koan_handler.cpp
)

add_subdirectory(koans)
include_directories(headers)

add_executable(cppkoans
  ${cppkoans_SOURCES}
)
