cmake_minimum_required(VERSION 3.5)

project(spdlog_vendor)

find_package(ament_cmake REQUIRED)

# Avoid DOWNLOAD_EXTRACT_TIMESTAMP warning for CMake >= 3.24
if(POLICY CMP0135)
  cmake_policy(SET CMP0135 NEW)
endif()

find_package(spdlog REQUIRED)

# this ensures that the package has an environment hook setting the PATH
ament_package()
