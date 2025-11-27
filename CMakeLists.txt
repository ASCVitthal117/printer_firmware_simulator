cmake_minimum_required(VERSION 3.10)
project(PrinterFirmwareDemo)

set(CMAKE_CXX_STANDARD 17)

add_executable(printer src/main.cpp src/printer.cpp)

enable_testing()
add_executable(/home/runner/work/printer_firmware_simulator/printer_firmware_simulator)
target_include_directories(test_printer PRIVATE ${CMAKE_SOURCE_DIR}/src)
find_package(GTest REQUIRED)
target_link_libraries(test_printer GTest::GTest GTest::Main)
include(GoogleTest)
gtest_discover_tests(test_printer)
