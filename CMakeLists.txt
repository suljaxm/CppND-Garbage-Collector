cmake_minimum_required(VERSION 2.6)
project(garbage_collector)

include_directories(include)
file(GLOB SOURCES "src/*.cpp")

add_executable(garbage_collector ${SOURCES})

set_property(TARGET garbage_collector PROPERTY CXX_STANDARD 17)

# TODO: Run -Werror in CI.
target_compile_options(garbage_collector PRIVATE -Wall -lncurses)
