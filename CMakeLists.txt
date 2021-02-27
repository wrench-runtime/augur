cmake_minimum_required(VERSION 3.6)
set(wrench_module augur)
project(${wrench_module})


# Copy script file to binary folder
configure_file(${CMAKE_CURRENT_SOURCE_DIR}/${wrench_module}.wren ${CMAKE_RUNTIME_OUTPUT_DIRECTORY}/${wrench_module}.wren COPYONLY)

