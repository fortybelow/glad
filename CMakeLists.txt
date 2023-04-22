cmake_minimum_required(VERSION 3.22)

project(Glad)

add_library(glad STATIC
    ${CMAKE_CURRENT_LIST_DIR}/src/glad.c
    ${CMAKE_CURRENT_LIST_DIR}/include/glad/glad.h
    ${CMAKE_CURRENT_LIST_DIR}/include/KHR/khrplatform.h
)

# Add path to glad headers
target_include_directories(glad PUBLIC include)

SET(GLAD_INCLUDE_DIR "${CMAKE_CURRENT_LIST_DIR}/include" CACHE INTERNAL "Glad include directory")
SET(GLAD_LIBRARIES glad CACHE INTERNAL "Glad libraries")
