# See also http://stackoverflow.com/a/18697099
cmake_minimum_required (VERSION 2.8.11)
project (main)
set(COOLPROP_STATIC_LIBRARY true)
add_subdirectory ("${CMAKE_SOURCE_DIR}/externals/CoolProp" CoolProp)
add_executable (main "${CMAKE_SOURCE_DIR}/mycode.cpp")
target_link_libraries (main CoolProp)