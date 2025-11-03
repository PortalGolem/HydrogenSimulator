cmake_minimum_required(VERSION 3.23)

project(HydrogenSimulator)

set(CMAKE_RUNTIME_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/$<CONFIGURATION>")
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/$<CONFIGURATION>")

add_subdirectory(vendored/SDL EXCLUDE_FROM_ALL)

add_executable(HydrogenSimulator)

target_sources(HydrogenSimulator
  PRIVATE
    main.c
)

target_link_libraries(HydrogenSimulator PRIVATE SDL3::SDL3)
