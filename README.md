# tangnano9k-sbc8080-light8080
SBC8080-like computer implemented on Tang Nano 9K using light8080 CPU core

- SBC8080 style computer made with Tang Nano 9K.
- Use light8080 (https://github.com/jaruiz/light8080) for 8080 core. The peripheral part is also based on the included mcu sample code.
- Modified the above mcu sample code so that Denno Densetsu (@vintagechips)'s program for SBC8080 can be run as is (binary compatible).
- The HEX file included in sbc8080_datapack seems to work for now.

## How to compile, etc.
- It seems that if you compile the whole sbc8080_project folder as a Gowin EDA project, it will work.
- Communication is 9600baud, 8bit, no parity, 1bit, none.
- src/mcu/ROM/obj_code_pkg.vhdl is embedded as ROM data from 0000H to 7FFFH. (By default, vhdl generated from MSBAS80.HEX is placed.)
- For conversion from other HEX files to vhdl,
See [sbc8080_project/src/mcu/ROM/README_JP.md](sbc8080_project/src/mcu/ROM/README_JP.md).
- I think that *.vhdl in the ROM folder should be usable as is if renamed to obj_code_pkg.vhdl.
- S1 and S2 buttons are reset buttons.
- One of the LEDs blinks at 4Hz, and the others only display a part of the address bus every 1/8, so there is no particular meaning.

## Modified contents of mcu related code
- Divided memory into 16KB ROM and 32KB RAM (Because Tang Nano 9K didn't have enough resources to secure 64KB all together.)
- Simplification of memory-related programs (removal of automatic size adjustment, etc.)
- Removed interrupt-related code (mcu_irq.vhdl)
- Fixed a bug-like part in clearing RXDRDY
- Simplify mcu_uart.vhdl (remove irq related)

## Other notes etc.
- Since the UART implements only minimal communication functions, writing to the 8251's control registers is ignored.
- This document was translated from the [Japanese original](README.jp.md) using Google Translate.