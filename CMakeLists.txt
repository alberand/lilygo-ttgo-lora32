# Find Zephyr. This also loads Zephyr's build system.
cmake_minimum_required(VERSION 3.13.1)

set(BOARD_ROOT ${CMAKE_CURRENT_LIST_DIR})

set(BOARD lilygo_ttgo_lora32)
find_package(Zephyr REQUIRED HINTS $ENV{ZEPHYR_BASE})
project(ttgo-zephyr)

# Add your source file to the "app" target. This must come after
# find_package(Zephyr) which defines the target.
target_sources(app PRIVATE src/main.c)
