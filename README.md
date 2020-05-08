# Olchanowski
## Fixing the Zortrax M200 electronics
The Zortrax M200's mechanical design is great. It's electronics and software is not.
Let's fix that!

### Checklist
- [X] Processor
- [X] 4 stepper drivers
- [X] Ethernet
- [X] Fan control
- [X] 3 end stops
- [X] "senser"
- [X] RGB LED strip control
- [X] Heated bed
  - [X] Driver
  - [X] Thermocouple
- [X] Power input
- [X] Power regulation
- [X] USB
- [X] UI cable
  - [X] Connector
  - [X] OLED panel (UG-5664ALBEF01)
  - [X] Beeper
  - [X] Rotary encoder
  - [X] SD card
- [X] Extruder cable
  - [X] Connector (1-281742-2)
  - [X] Stepper
  - [X] Heater
  - [X] Thermocouple
  - [X] Fans
- [X] ICSP: UART
- [X] Filament sensor
- [X] LEDs
  - [X] GPIOs
  - [X] Voltage rail
  - [X] Heaters

## Version 1: Order list
| Description                                | MPN                   | QTY |
|--------------------------------------------|-----------------------|-----|
| Extruder cable connector                   | 1-281742-2            | 1   |
| Heated bed connector                       | 1744428-4             | 1   |
| LCD connector                              | 302-S201              | 1   |
| Ethernet jack                              | ARJM11D7-009-AB-ER2-T | 1   |
| End switch + FAN + HB thermistor connector | B2B-XH-AM(LF)(SN)     | 5   |
| Diode                                      | BAT60AE6327HTSA1      | 2   |
| 470pF 0402                                 | C0402C471K5RACTU      | 2   |
| 22nF 0402                                  | GRM155R71H223KA12J    | 4   |
| 100 Ohm 0402                               | CRG0402F100R          | 2   |
| 10 kOhm 0402                               | CRG0402F10K           | 26  |
| 1 kOhm 0402                                | CRG0402F1K            | 3   |
| 1.5 kOhm 0402                              | CRG0402F1K5           | 2   |
| 1 Mohm 0402                                | CRG0402F1M            | 1   |
| 22 Ohm 0402                                | CRG0402F22R           | 4   |
| 2.4 kOhm 0402                              | CRG0402F2K4           | 1   |
| 33 Ohm 0402                                | CRG0402F33R           | 2   |
| 4.7 kOhm 0402                              | CRG0402F4K7           | 2   |
| 50 Ohm 0402                                | CRG0402F50R           | 4   |
| 12MHz crystal                              | CX3225SB12000H0PSTC1  | 1   |
| 25MHz crystal                              | CX3225SB25000H0FLJCC  | 1   |
| 12.1 kOhm                                  | ERJ-2RKF1212X         | 1   |
| Push buttons                               | EVQ-Q2Y03W            | 2   |
| 12pF 0402                                  | GRM1555C1E120GA01D    | 10  |
| 4.7uF 0402                                 | GRM155R61A475MEAAD    | 13  |
| 100nF 0402                                 | GRM155R61H104KE19D    | 45  |
| 10uF 0805                                  | GRM21BR6YA106ME43L    | 8   |
| Current sense resistor 0.1 Ohm 1206        | KRL1632E-M-R100-F-T5  | 8   |
| LM5551                                     | LM5111-1MX/NOPB       | 1   |
| LPC1768                                    | "LPC1769FBD100,551"   | 1   |
| LEDs 0603                                  | LTST-C190TBKT         | 7   |
| Inductor                                   | MLZ1608A1R0WT000      | 1   |
| PCA9306DCTR                                | PCA9306DCTR           | 1   |
| 6 pin header                               | PPTC061LFBN-RC        | 1   |
| Power MOSFET                               | SIJA58DP              | 2   |
| N-Ch MOSFET                                | "SSM3K329R,LF"        | 6   |
| Stepper driver                             | TMC2209-LA            | 4   |
| 220uF elcaps                               | UCW1V221MNL1GS        | 8   |
| Stepper + RGB + filament sensor connectors | B4B-XH-A(LF)(SN)      | 5   |
| USB-C female connector                     | DX07S024XJ1R1100      | 1   |
| Power connector                            | 282814-4              | 1   |
| Power module                               | TPSM53602             | 1   |
| P-Ch MOSFET                                | DMP3099L-13           | 1   |
| Ethernet PHY                               | LAN8720A-CP-TR-ABC    | 1   |
| Inverter                                   | 74HC1G04              | 1   |
| 3.3V regulator                             | NCP5661MN33T2G        | 1   |
| Senser connector                           | B3B-XH-A(LF)(SN)      | 1   |
