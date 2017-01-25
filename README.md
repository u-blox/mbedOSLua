This repository contains a ludicrously simple port of Lua to mbedOS.

Prerequisites
=============
- mbed CLI and a compiler for it (ARM, GCC_ARM or IAR),
- a board that supports mbedOS (I chose the Freedom K64F board).

How This Repo Should Be Used
============================
- Clone this repo with git clone https://github.com/u-blox/mbedOSLua.git.
- Run `mbed update` to retrieve the mbedOS source code.
- Run `mbed compile`, giving it your choice of target and compiler, e.g. `mbed compile -m K64F -t ARM`.
- Copy the resulting `.bin` onto your board.
- Open a terminal to the board with the following settings:
  - baud rate 9600
  - no flow control
  - local echo ON
  - line-ending that is SENT set to LF; note that PuTTY *cannot* be persuaded to do this, Teraterm can.
- Reset the board and you should get a Lua prompt.
- Type characters and they will be interpreted as Lua commands, e.g. `"print("Hello World")"`.

How This Repo Was Created
=========================
- Create an empty mbedOS Lua build with:

 `mkdir mbedOSlua`
 
 `cd mbedOSlua`
 
 `mbed new .`

- Download the latest version of the Lua source code from https://www.lua.org/ftp/ (the version here is 5.3.3).
- Unzip this into the `mbedOSlua` directory created above.
- That's it.