# Defines the minimum version of cmake required for the project
cmake_minimum_required(VERSION 3.16)

# Tells cmake the name of the project and can specify the language as well (CXX = C++)
project(Timber LANGUAGES CXX)

# Tells cmake to compile the code using C++ version 20
set(CMAKE_CXX_STANDARD 20)

# Tells cmake that C++ version 20 is required and not to fall back on an older version of C++
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Tells cmake what external libraries we need (Here we are using SFML version 2.6 or compatible
# and we need SFML graphics, window, system and audio components)
find_package(SFML 2.6 COMPONENTS graphics window system audio REQUIRED)

# Tells cmake to create an executable file called Timber using src/Timber.cpp (Timber.cpp contains our main method)
add_executable(Timber
    src/Timber.cpp
)

# Tells cmake to link these listed libraries when building the Timber executable, Timber is the target
target_link_libraries(Timber
    sfml-graphics
    sfml-window
    sfml-system
    sfml-audio
)
