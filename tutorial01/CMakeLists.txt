cmake_minimum_required (VERSION 2.6)
project (leptjson_test C)
if (CMAKE_C_COMPILER_ID MATCHES "GNU|Clang")
    set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -ansi -pedantic -Wall")
endif()
add_library(leptjson
        leptjson.c
        test.c)
target_include_directories(leptjson INTERFACE ${CMAKE_CURRENT_SOURCE_DIR})