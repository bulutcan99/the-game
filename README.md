<div align="center">
  <img
    alt="chip-8"
    src="https://csdb.dk/gfx/releases/17000/17306.png"
    height="300px"
  />
</div>

# Chip-8 Emulator
A Chip-8 emulator written in Rust that uses SDL2.

# Sources
|http://devernay.free.fr/hacks/chip8/C8TECH10.HTM#8xy3|Chip-8 technical information.|
|https://github.com/rodrigoCucick/rusted-chip8|Chip-8 coding reference while developing the Chip-8 emulator in Rust.|
|https://github.com/mattmikolay/chip-8/wiki/CHIP%E2%80%908-Instruction-Set|Another Chip-8 technical reference with some additional information.|

# Current Features
As it is, the emulator is fully functional and capable of executing any Chip-8 game based on the original instruction set.

Some videos of it can be found here: https://www.youtube.com/c/RodrigoCucick

__Macro features:__
|Feature|Implemented?|
|--|--|
|Instructions (CPU)|Yes|
|Memory|Yes|
|Input|Yes|
|Display|Yes|
|Audio (buzzer)|Yes|

__Individual instructions:__
|Instruction|Implemented?|
|--|--|
|`0000` - NOP|Not used|
|`00E0` - CLS|Not used|
|`00EE` - RET|Not used|
|`0NNN` - SYS addr|Not used|
|`1NNN` - JP addr|Not used|
|`2NNN` - CALL addr|Not used|
|`3XKK` - SE VX, byte|Not used|
|`4XKK` - SNE VX, byte|Not used|
|`5XY0` - SE VX, VY|Not used|
|`6XKK` - LD VX, byte|Not used|
|`7XKK` - ADD VX, byte|Not used|
|`8XY0` - LD VX, VY|Not used|
|`8XY1` - OR VX, VY|Not used|
|`8XY2` - AND VX, VY|Not used|
|`8XY3` - XOR VX, VY|Not used|
|`8XY4` - ADD VX, VY|Not used|
|`8XY5` - SUB VX, VY|Not used|
|`8XY6` - SHR VX {, VY}|Not used|
|`8XY7` - SUBN VX, VY|Not used|
|`8XYE` - SHL VX {, VY}|Not used|
|`9XY0` - SNE VX, VY|Not used|
|`ANNN` - LD I, addr|Not used|
|`BNNN` - JP V0, addr|Not used|
|`CXKK` - RND VX, byte|Not used|
|`DXYN` - DRW VX, VY, nibble|Not used|
|`EX9E` - SKP VX|Not used|
|`EXA1` - SKNP VX|Not used|
|`FX07` - LD VX, DT|Not used|
|`FX0A` - LD VX, K|Not used|
|`FX15` - LD DT, VX|Not used|
|`FX18` - LD ST, VX|Not used|
|`FX1E` - ADD I, VX|Not used|
|`FX29` - LD F, VX|Not used|
|`FX33` - LD B, VX|Not used|
|`FX55` - LD [I], VX|Not used|
|`FX65` - LD VX, [I]|Not used|

# Keyboard
The keyboard inputs are mapped to the following keys:

__Emulator layout__:
|||||
|--|--|--|--|
|1|2|3|4|
|Q|W|E|R|
|A|S|D|F|
|Z|X|C|V|

__Original ASCII layout (_for reference only_):__
|||||
|--|--|--|--|
|1|2|3|C|   
|4|5|6|D|   
|7|8|9|E|   
|A|0|B|F|

# Settings
The emulator also has an external configuration file called `config.yaml`, where it is possible to adjust some settings like:
1. Video resolution scale.
2. Instruction cycles per frame.
3. Color (background and pixel).
