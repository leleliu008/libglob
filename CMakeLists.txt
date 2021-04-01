cmake_minimum_required(VERSION 3.0.0)

add_library(glob_a STATIC glob.c)
add_library(glob   SHARED glob.c)

include(GNUInstallDirs)

install(TARGETS glob LIBRARY                      DESTINATION ${CMAKE_INSTALL_LIBDIR})
install(FILES   ${PROJECT_BINARY_DIR}/libglob_a.a DESTINATION ${CMAKE_INSTALL_LIBDIR})
install(FILES   ${PROJECT_SOURCE_DIR}/glob.h      DESTINATION ${CMAKE_INSTALL_INCLUDEDIR})
