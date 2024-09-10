cmake_minimum_required(VERSION 3.18...3.22)

project(${SKBUILD_PROJECT_NAME} LANGUAGES C)

find_package(Python COMPONENTS Interpreter Development.Module REQUIRED)

Python_add_library(GeoIP MODULE py_GeoIP.c WITH_SOABI)
install(TARGETS GeoIP DESTINATION .)
