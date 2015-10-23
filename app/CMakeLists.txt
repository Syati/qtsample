cmake_minimum_required(VERSION 2.8.11)

project(sample)

# make frag
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11 -stdlib=libc++ -Wall -pedantic -Wextra -Wnon-virtual-dtor -Woverloaded-virtual")
set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTOUIC ON)

# for include path
set(CMAKE_INCLUDE_CURRENT_DIR ON)

# Find libraries
find_package(Qt5Widgets REQUIRED)
find_package(Qt5Core REQUIRED)
find_package(Qt5Gui REQUIRED)
find_package(Qt5Designer REQUIRED)
find_package(Qt5Test REQUIRED)

enable_testing()

add_subdirectory(src)
add_subdirectory(tests)

