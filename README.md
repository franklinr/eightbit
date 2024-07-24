# Eightbit

This is a repository of various bits of code related to my version of [Ben Eater's 8-bit computer](https://eater.net/8bit/).  This is mainly to remind me what I have done, but maybe it is useful for others too.  Here is a video of the [computer computing the Fibonacci sequence](https://www.youtube.com/watch?v=IHi4pi4AkN4).

![](img/eightbit.png)

One of the main differences is in the bus and control logic.  [Ben Eater's control logic](https://www.youtube.com/watch?v=FCscQGBIL-Y) controls individual binary signals for each component that is connected to the bus.  In my computer, I have one output decoder with three bits that control which component is outputting to the bus and another decoder with four bits that controls which component is inputting to the bus. 

| Number | Output Instruction   | Name OUT |   | Name IN              | Name IN |
|--------|----------------------|----------|---|----------------------|---------|
| 0      | No operation         | NOP      |   | No operation         | NOP     |
| 1      | Register B           | BO       |   | Register B           | BI      |
| 2      | ALU                  | EO       |   | Register A           | AI      |
| 3      | Register A           | AO       |   | Instruction Register | II      |
| 4      | Instruction Register | IO       |   | Display              | OUT     |
| 5      | Program Counter      | CO       |   | Memory Register      | MI      |
| 6      | Memory Register      | MO       |   | RAM                  | RI      |
| 7      | RAM                  | RO       |   | JUMP                 | J       |

You can see how it functions [here](https://www.youtube.com/watch?v=CHGl77YNiHg).  With these decoders, you only need one eeprom to control the computer (as opposed to the two that Ben uses).

- [Yet Another EEPROM programmer](https://github.com/franklinr/eightbit/blob/cedbab8e126954b938e39369f0d79d1743543633/Yet_Another_EEPROM_programmer/Readme.md):  This is an EEPROM programmar for the AT28C16/sst39sf0 chips with a simple wiring scheme and serial monitor program.
