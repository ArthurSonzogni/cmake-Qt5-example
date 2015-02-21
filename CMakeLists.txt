# ┌──────────────────────────────────────────────────────────────────┐
# │  Projects Settings                                               │
# └──────────────────────────────────────────────────────────────────┘

cmake_minimum_required(VERSION 2.8.11)
project(myApplication)

# ┌──────────────────────────────────────────────────────────────────┐
# │  Qt                                                              │
# └──────────────────────────────────────────────────────────────────┘

set(CMAKE_INCLUDE_CURRENT_DIR ON)
set(CMAKE_AUTOMOC ON)
find_package(Qt5Widgets REQUIRED)

# ┌──────────────────────────────────────────────────────────────────┐
# │  Source file                                                     │
# └──────────────────────────────────────────────────────────────────┘

file(GLOB_RECURSE source src/*.cpp)
include_directories(src)

# ┌──────────────────────────────────────────────────────────────────┐
# │  Applications  (entry points)                                    │ 
# └──────────────────────────────────────────────────────────────────┘

# FractalCreation
add_executable(myApplication app/myApplication.cpp ${source})
qt5_use_modules(myApplication Widgets)
