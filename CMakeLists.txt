cmake_minimum_required(VERSION 2.6.0)
PROJECT(cv)
SET(CMAKE_INCLUDE_CURRENT_DIR ON)                                                                                                                                                   
FIND_PACKAGE(Curses REQUIRED)
file(GLOB srcx
    "*.c"
)

SET(cv_SOURCES ${srcx})
INCLUDE_DIRECTORIES(${CURSES_INCLUDE_DIR})
ADD_EXECUTABLE(cv ${cv_SOURCES})
target_link_libraries(cv ${CURSES_LIBRARIES})
target_link_libraries(cv m)
