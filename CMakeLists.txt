cmake_minimum_required(VERSION 3.1...3.29)

project(
  Crystal
  VERSION 1.0
  LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

set(CMAKE_TOOLCHAIN_FILE "X:/vcpkg/scripts/buildsystems/vcpkg.cmake")
set(VCPKG_TARGET_TRIPLET "x64-windows")

set(Qt6_DIR "X:\\vcpkg\\installed\\x64-windows\\share\\Qt6")

find_package(Qt6 REQUIRED COMPONENTS Core)
qt_standard_project_setup()

qt_add_executable(Crystal src/main.cpp)

target_link_libraries(Crystal PRIVATE Qt6::Core)