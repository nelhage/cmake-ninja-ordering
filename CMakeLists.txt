cmake_minimum_required(VERSION 3.10)

project(Debug)

add_custom_command(
  OUTPUT greeting.cxx
  COMMAND ${CMAKE_CURRENT_SOURCE_DIR}/make_greeting.sh
)
add_executable(main
  main.cxx
  greeting.cxx
  greeting.h
)
