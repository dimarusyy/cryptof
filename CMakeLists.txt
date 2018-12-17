cmake_minimum_required (VERSION 3.10)

message(STATUS "cmake version: ${CMAKE_VERSION}")
project(cryptof LANGUAGES CXX)
include(CTest)

set(CXX_STANDARD_REQUIRED ON)
message(STATUS "CMAKE_CXX_STANDARD=${CMAKE_CXX_STANDARD}")