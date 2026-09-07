cmake_minimum_required(VERSION 3.16)

project(Timber)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(SFML 2.6 COMPONENTS graphics window system audio REQUIRED)

add_executable(Timber
    src/Timber.cpp
)

target_link_libraries(Timber
    sfml-graphics
    sfml-window
    sfml-system
    sfml-audio
)
