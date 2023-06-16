## What's in this directory
- README_JP.md: this file
- bin2vhdl.c: program to generate vhdl from binary files
- bin2vhdl.exe: bin2vhdl.c compiled with cygwin's gcc
- MSBAS80.obj_code_pkg.vhdl: vhdl file created from MSBAS80.HEX
- MON80SA.obj_code_pkg.vhdl: vhdl file made from MON80SA.HEX
- TEST80.obj_code_pkg.vhdl: vhdl file created from TEST80.HEX
- PTBEXSA.obj_code_pkg.vhdl: vhdl file created from PTBEXSA.HEX
- obj_code_pkg.vhdl: same as MSBAS80.obj_code_pkg.vhdl
- ASCIIART.BAS: Mandelbrot set display program for MSBAS80
- Makefile: (for reference)

## How to create obj_code_pkg.vhdl from HEX file
- Create a 16KB binary file from HEX files such as MSBAS80.HEX included in sbc8080_datapack (please obtain separately). (I loaded and saved for 27256 with the ROM writer program (Xgpro).)
- bin2vhdl.exe MSBAS80.BIN > obj_code_pkg.vhdl to create a vhdl file.

## Other notes etc.
- This document was translated from the [Japanese original](README.jp.md) using Google Translate.