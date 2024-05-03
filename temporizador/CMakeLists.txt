add_executable(temporizador
                temporizador.c
                main_temp.c
        )     

# pull in common dependencies
target_link_libraries(temporizador pico_stdlib hardware_gpio hardware_timer)

# enable usb output, disable uart output
pico_enable_stdio_usb(temporizador 1)
pico_enable_stdio_uart(temporizador 0)

# create map/bin/hex file etc.
pico_add_extra_outputs(temporizador)

