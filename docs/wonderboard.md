# Wonderboard

## Objective
One standardized universal microcontroller board that can run any keyboard wirelessly. 

### Why?
Consolidating technical complexity to one standardized part means all boards may benefit from the same development effort. Troubleshooting, tooling, and supply chain become far simpler. Reduced process variation and development cost/time/effort enables faster and easier design of new keyboards/layouts/variants.

## Meet the Wonderboard

| Need                    | Solution                                                                                                                                                               |
| ----------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| All-in-one design       | Onboard MCU, BMS, 2x battery connectors, load switch, USB port, power switch, indicator LEDs, antenna                                                                  |
| Support for all layouts | Enough GPIOs for an ideal column-row setup for a "worst case" battleship board                                                                                         |
| Support for peripherals | Extra GPIOs, voltage and ground pins, toggleable voltage                                                                                                               |
| Reversible              | All non software-defined pins are to be mirrored (GND, Vdd, Vsw)                                                                                                       |
| Easy access             | Compact 40 pin ribbon cable to shield, all 40 pins broken out onto breadboard-like 2.54 mm (0.1 in) grid for handsoldered builds or for soldering directly to a shield |

### All-in-one design
Placing all core components onto the wonderboard provides two main benefits. Firstly, it allows for vastly simpler shields that act similar to a breakout board. This eases the design of variant shields with different layouts, hotswap/solder variants, LEDs, and more. Secondly, it takes advantage of economies of scale by having most of the high-cost assembly components on one universal board and removing the need for costly high-precision manufacturing tolerances on the shields. 

### Support for all layouts
The wonderboard exposes 34 GPIOs. This is more than enough for a fullsize 100% board and unique, large layouts like battleship boards (24 columns + 8 rows = 32 pins). A 17x17 matrix can be used to achieve a maximum of 289 keys.

### Support for peripherals
The inclusion of power pins and extra GPIOs grants support for peripheral components such as LEDs, displays, buzzers, solenoids, and more. The wonderboard provides ground and power in the form of regular voltage and toggleable voltage rails. Toggled voltage provides enormous energy savings when components are not needed. LEDs use multiple orders of magnitude more energy than the wonderboard itself. Where the MCU has a nominal consumption of a couple microwatts, a single SK6812 MINI-E LED uses up to 800mW and has a static consumption of 4mW (at 4V).

### Reversible
The wonderboard can be installed facing up or down. This is accomplished by having a "mirrored" ribbon cable pinout, where ground, voltage, and toggleable voltage are mirrored on either end and all GPIOs are in the center, where pin assignments can be redefined in firmware.

### Easy access
The wonderboard has its 40 pin output available as both a reversible ribbon cable and as a 2 by 20 pad array. This means that in addition to the suggested ribbon cable connection, handwired boards and directly soldered shields are compatible.

