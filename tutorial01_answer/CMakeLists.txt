cmake_minimum_required (VERSION 3.10)
project (leptjson_test VERSION 11)

if (CMAKE_C_COMPILER_ID MATCHES "GNU|Clang")
    set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -ansi -pedantic -Wall")
endif()

add_library(leptjson leptjson.c test.c)
target_include_directories(leptjson PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
#add_executable(leptjson_test test.c)
#target_link_libraries(leptjson_test leptjson)
