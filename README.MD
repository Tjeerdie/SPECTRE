# Project SPECTRE
Project SPECTRE	(Speeduino PrintEd Circuit board TjeeRdiE). This is a PCB with the hardware to run speeduino on a STM32F407VE6T board from ebay. (Or a STM32 BLACK_F407VE as it is sometimes called). Schematics and more information on the cpu board can be found here: (https://github.com/mcauser/BLACK_F407VE) The case with connectors can be found here: https://nl.aliexpress.com/item/32839361268.html?spm=a2g0z.12010615.8148356.7.1da330edPBhz16

Latest version is 0.5.2

A stand alone Peak and Hold injector driver board is now seperate. See: https://github.com/Tjeerdie/Peak-And-hold-Driver

## Getting Started
Take a look at the very iformative manual for speeduino:
https://speeduino.com/Speeduino_manual.pdf

How to load the firmware to the STM32 see:
https://speeduino.com/forum/viewtopic.php?f=13&t=1914&p=26572#p26572

## Board pinout:
| Pin# | Function    | Alternative | Switch |
|-----|-------------|-------------|--------|
| 1   | GND_PWR     |             |        |
| 2   | GND_PWR     |             |        |
| 3   | 12V_ECU     |             |        |
| 4   | 12V_ECU     |             |        |
| 5   | INJ_CH8     |             |        |
| 6   | INJ_CH7     |             |        |
| 7   | INJ_CH5     |             |        |
| 8   | INJ_CH6     |             |        |
| 9   | IDLE1-OUT   | STEP_1A_OUT | JP5    |
| 10  | BARO        |             |        |
| 11  | Spare_2_out | Step_2B_OUT | JP6    |
| 12  | Spare_1_Out | Step_1B_OUT | JP7    |
| 13  | IGN_CH1     |             |        |
| 14  | 02_2        |             |        |
| 15  | FAN         |             |        |
| 16  | IDLE2-OUT   | STEP_2A_OUT | JP8    |
| 17  | IAT         |             |        |
| 18  | IAT_2       |             |        |
| 19  | FUEL_PUMP   |             |        |
| 20  | CLT_2       |             |        |
| 21  | RS232_TX    |             |        |
| 22  | GND         | IGN5-OUT    | JP18   |
| 23  | O2          |             |        |
| 24  | INJ_CH4     |             |        |
| 25  | MAP         |             |        |
| 26  | GND         | IGN6-OUT    | JP16   |
| 27  | CLT         |             |        |
| 28  | INJ_CH3     |             |        |
| 29  | CANH        |             |        |
| 30  | GND         |             |        |
| 31  | IGN_CH2     |             |        |
| 32  | INJ_CH1     |             |        |
| 33  | GND         |             |        |
| 34  | RS232_RX    |             |        |
| 35  | TPS         |             |        |
| 36  | IGN_CH3     |             |        |
| 37  | 5V          |             |        |
| 38  | FLEX_IN     |             |        |
| 39  | VR2-        |             |        |
| 40  | IGN_CH4     |             |        |
| 41  | VR2+        |             |        |
| 42  | VR1-        |             |        |
| 43  | VR1+        |             |        |
| 44  | INJ_CH2     |             |        |
| 45  | CANL        |             |        |
| 46  | 3.3V        |             |        |
| 47  | BOOST-OUT   |             |        |
| 48  | TACHO-OUT   |             |        |


## Tested on V0.5.2
The following functions have been tested and confirmed to be working with real under the bonnet hardware and provide good results. An 4 cylinder engine with wasted spark is running on this hardware<br/> 
VR2 input (Trigger 2) [OK]<br/> 
Halleffect trigger input (Trigger 1) [OK]<br/>
VR1 input (Trigger 1) [OK] <br/> 
Halleffect trigger input (Trigger 2) [OK]<br/>
Manifold Absolute pressure (MAP) [OK]<br/>
Injector outputs [OK]<br/>
Lambda sensor (O2) [OK]<br/>
Throttle position input [OK]<br/>
Bluetooth module (PA9,PA10) [OK]<br/>
Battery voltage reading [OK]<br/> 
Ignition outputs [OK]<br/> 
Fuel pump relay [OK]<br/>
FAN relay [OK]<br/>
PWM idle output [OK]<br/>
Coolant temperature (CLT) [OK]<br/>
Inlet Air Temperature (IAT) [OK]<br/>
RS232 TX [OK]<br/>
RS232 RX [OK]<br/>

## To be tested on V0.5.2
TACHO out<br/>
BOOST output<br/>
Stepper idle output<br/> 
BARO <br/>
CAN bus TX<br/>
CAN bus RX<br/>
FLEX fuel input<br/>
Coolant temperature (CLT_2) <br/>
Inlet Air Temperature (IAT_2) <br/>
Lambda sensor (O2_2) <br/>



## License
This project is licensed under the GNU GENERAL PUBLIC LICENSE - see the [LICENSE.md](LICENSE.md) file for details


