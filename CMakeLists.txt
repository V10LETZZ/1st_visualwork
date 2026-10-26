cmake_minimum_required(VERSION 3.16)
project(robomaster_vision_training VERSION 0.1.0 LANGUAGES CXX)

add_executable(cmake_1st cmake_1st.cpp)
target_compile_features(cmake_1st PRIVATE cxx_std_17)
set_target_properties(cmake_1st PROPERTIES CXX_EXTENSIONS OFF)

if(MSVC)
    target_compile_options(cmake_1st PRIVATE /W4 /permissive-)
else()
    target_compile_options(cmake_1st PRIVATE -Wall -Wextra -Wpedantic)
endif()
