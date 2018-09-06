cmake_minimum_required(VERSION 3.5.1)

project(QtPaint)

#Set path to your Qt5 directory
set(CMAKE_PREFIX_PATH  "/home/jin/Qt/5.11.2/gcc_64/")

#Find includes in corresponding build directories
set(CMAKE_INCLUDE_CURRENT_DIR ON)

#Instruct CMake to run moc automaticaly when needed
set(CMAKE_AUTOMOC ON)

#Create code from a list of Qt designer ui files
set(CMAKE_AUTOUIC ON)

#Find the QtWidgets library
find_package(Qt5Widgets CONFIG REQUIRED)

#Pupulate a CMake variable with the sources
set(srcs mainwindow.ui mainwindow.cpp main.cpp)

#Tell CMake to create QtPaint executable
add_executable(QtPaint ${srcs})

#Use the Widgets module from Qt 5
target_link_libraries(QtPaint Qt5::Widgets)