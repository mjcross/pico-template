cmake_minimum_required(VERSION 3.5)

# === set the name of your project here ===
set(ProjectName Hello_World)
# =========================================

include(pico_sdk_import.cmake)

project(${ProjectName})

pico_sdk_init()

add_compile_options(
	-Wall
	-Wno-format
	-Wno-unused-function
	-Wno-maybe-uninitialized
	-Wextra    			# optional
)

add_executable(${ProjectName}    
    main.c
)

pico_enable_stdio_usb(${ProjectName} 0)
pico_enable_stdio_uart(${ProjectName} 1)

pico_add_extra_outputs(${ProjectName})

target_link_libraries(${ProjectName} pico_stdlib)
