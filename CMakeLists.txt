cmake_minimum_required(VERSION 3.20)

project(chat-leader-gui VERSION 1.0.0)

set(CMAKE_INCLUDE_CURRENT_DIR ON)

# Turn on automatic invocation of the MOC, UIC & RCC
set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTOUIC ON)
set(CMAKE_AUTORCC ON)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wall")

find_package(Qt5 REQUIRED COMPONENTS Widgets)

# Create the executable
add_executable(${PROJECT_NAME} main.cpp mainwindow.cpp mainwindow.ui)

target_link_libraries(${PROJECT_NAME} Qt5::Widgets)
