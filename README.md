# eightbit

This is a repository of various bits of code related to building a Ben Eater style 8-bit computer.
https://eater.net/8bit/

- [Yet Another EEPROM programmer](https://github.com/franklinr/eightbit/tree/365b3baa6161d407396759152b12193fe1314522/Yet_Another_EEPROM_programmer):  This is an EEPROM programmar for the AT28C16/sst39sf0 chips with a simple wiring scheme and serial monitor program.



[Ben Eater's control logic](https://www.youtube.com/watch?v=FCscQGBIL-Y) involves individual binary signals for each component that is connected to the bus.  [In my computer](https://www.youtube.com/watch?v=CHGl77YNiHg), I have one output decoder with three bits that control which component is outputting to the bus and another decoder with four bits that controls which component is inputting to the bus.

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
