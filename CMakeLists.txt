cmake_minimum_required(VERSION 2.8)
project(smartcarsim)
include_directories(scs/include)
add_subdirectory(scs)

add_executable(demo demo/demo.cpp)
target_link_libraries(demo 
    scs 
    GL 
    GLU 
    glut 
    ode 
    pthread)

set(CMAKE_INSTALL_PREFIX "${CMAKE_SOURCE_DIR}/bin")
install(DIRECTORY tracks DESTINATION "${CMAKE_INSTALL_PREFIX}")
install(TARGETS demo RUNTIME DESTINATION "${CMAKE_INSTALL_PREFIX}")