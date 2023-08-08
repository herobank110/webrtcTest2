cmake_minimum_required(VERSION 3.14 FATAL_ERROR)

project(WebrtcTest2)

include(./cmake/CPM.cmake)
CPMAddPackage("gh:ericniebler/range-v3#0.12.0")

add_executable(WebrtcTest2 main.cpp)
target_compile_features(WebrtcTest2 PRIVATE cxx_std_20)
target_link_libraries(WebrtcTest2 range-v3)
