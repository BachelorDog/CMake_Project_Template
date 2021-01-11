cmake_minimum_required(VERSION 3.10)
cmake_policy(SET CMP0004 NEW)

add_compile_options(-O3 -W -Wall -Werror -g)

set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_SOURCE_DIR}/bin)
set(CMAKE_CXX_FLAGS "-Wno-unused-parameter ${CMAKE_CXX_FLAGS}")

add_subdirectory(src/app)
add_subdirectory(src/include)
add_subdirectory(src/lib)

