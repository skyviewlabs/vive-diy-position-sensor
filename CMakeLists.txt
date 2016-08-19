cmake_minimum_required(VERSION 3.5)

set(CMAKE_TOOLCHAIN_FILE "teensy-arm.toolchain.cmake")
set(CMAKE_DISABLE_SOURCE_CHANGES ON)
#set(CMAKE_VERBOSE_MAKEFILE TRUE)

project(lighthouse_teensy)

set(SOURCE_FILES
        main.cpp
        setup.cpp
        data_decoder.cpp
        geometry.cpp
)

add_executable(lighthouse-teensy "${SOURCE_FILES}")

add_firmware_targets(lighthouse-teensy)
# import_arduino_library(lighthouse-teensy ADC)