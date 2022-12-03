cmake_minimum_required(VERSION 3.2)

set(PATCH_VERSION "1" CACHE INTERNAL "Patch version")
set(PROJECT_VESRION 0.0.${PATCH_VERSION})
project(yatzyext VERSION ${PROJECT_VESRION})

add_executable(datarace datarace.cpp)
add_executable(heartbleed heartbleed.c)
add_executable(useafterfree useafterfree.cpp)

set_target_properties(datarace heartbleed useafterfree PROPERTIES
    CXX_STANDARD 14
    CXX_STANDARD_REQUIRED ON
)
