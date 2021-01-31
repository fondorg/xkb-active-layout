cmake_minimum_required(VERSION 3.17)
project(xkb_active_layout C)

set(CMAKE_C_STANDARD 11)
include(FindX11)
add_executable(xkb_active_layout main.c)
target_link_libraries(xkb_active_layout ${X11_LIBRARIES})
target_link_libraries(xkb_active_layout
        /usr/lib/x86_64-linux-gnu/libxkbfile.a)
