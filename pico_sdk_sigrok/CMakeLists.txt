cmake_minimum_required(VERSION 3.13)

# include(pico_sdk_import.cmake)

# include(pico_extras_import_optional.cmake)

#project(test_project C CXX ASM)
#set(CMAKE_C_STANDARD 11)
#set(CMAKE_CXX_STANDARD 17)
#pico_sdk_init()

add_executable(pico_sdk_sigrok
  pico_sdk_sigrok.c
)

pico_enable_stdio_usb(pico_sdk_sigrok 1)
pico_enable_stdio_uart(pico_sdk_sigrok 0)

pico_add_extra_outputs(pico_sdk_sigrok)

target_link_libraries(
    pico_sdk_sigrok 
    pico_stdlib
    hardware_adc
    hardware_dma
    hardware_pio
    hardware_sync
    pico_multicore
    pico_stdio_usb
		pico_stdio
		hardware_clocks
		hardware_base
		hardware_structs
		hardware_regs
		pico_binary_info		
)
# tinyusb is implicit
