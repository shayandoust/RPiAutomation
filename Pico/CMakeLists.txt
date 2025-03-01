cmake_minimum_required(VERSION 3.30)

### pico-sdk
set(PICOTOOL_FETCH_FROM_GIT_PATH, "external/")
include(external/pico-sdk/pico_sdk_init.cmake)

pico_sdk_init()
###

project(Pico CXX C ASM)
set(CMAKE_CXX_STANDARD 26)

add_executable(Pico test.cpp)

target_link_libraries(Pico pico_stdlib)
pico_add_extra_outputs(Pico)