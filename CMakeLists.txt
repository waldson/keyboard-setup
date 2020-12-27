cmake_minimum_required(VERSION 3.0)

project(w5n-keymappings)

add_executable(w5n-keymappings src/keyboard-mappings.c)
target_compile_options(w5n-keymappings PRIVATE -Wall -Wextra)

install(TARGETS w5n-keymappings RUNTIME DESTINATION bin)
