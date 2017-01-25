This repository contains a ludicrously simple port of Lua to mbedOS.

Prerequisites
=============
- mbed CLI and a compiler for it (ARM, GCC_ARM or IAR),
- a board the supports mbedOS (I chose the Freedom K64F board).

How This Was Created
====================
- Create an empty mbedOS Lua build with:

 `mkdir lua`
 
 `cd lua`
 
 `mbed new .`

- Download the latest version of the Lua source code from https://www.lua.org/ftp/ (the version here is 5.3.3).
- Unzip this into the `lua` directory created above.

How This Repo Should Be Used
============================
- Change to the directory `lua` you created above.
- Run `mbed update` to retrieve the latest mbedOS source code.
- Run `mbed compile`, giving it your choice of target and compiler.
- Copy the resulting binary onto your board.
- Open a terminal to the board with the following settings:
  - baud rate 9600
  - no flow control
  - local echo ON
  - line-ending that is SENT set to LF; note that PuTTY *cannot* be persuaded to do this, Teraterm can.
- Reset the board and you should get a Lua prompt.
- Type characters and they will be interpreted as Lua commands.