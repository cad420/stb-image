cmake_minimum_required(VERSION 3.0)
project(stbi)

add_library(stbi src/stbi_impl.cc)
target_include_directories(stbi PUBLIC 
  ${CMAKE_CURRENT_SOURCE_DIR}/include
)
