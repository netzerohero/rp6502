cmake_minimum_required(VERSION 3.13)

project(MY-RP6502-PROJECT C ASM)

add_subdirectory(rp6502-sdk)

add_executable(tetricks)
rp6502_executable(tetricks)
target_sources(tetricks PRIVATE
    src/tetricks.c
    src/bitmap_graphics.c
)
target_link_libraries(tetricks PRIVATE
    rp6502
)

