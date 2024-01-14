# Project SPECTRE
Project SPECTRE	(Speeduino PrintEd Circuit board TjeeRdiE). This is a PCB with the hardware to run speeduino on a STM32F407VE6T board from ebay. (Or a STM32 BLACK_F407VE as it is sometimes called). 

Schematics and more information on the cpu board can be found here: (https://github.com/mcauser/BLACK_F407VE)

The case with connectors can be found here: https://nl.aliexpress.com/item/32839361268.html?spm=a2g0z.12010615.8148356.7.1da330edPBhz16

Latest tested version by author is 0.5.3. Version 0.5.4 is a cleaned up schematic plus a change to use resistor arrays rather than individual resistors by @vitorboss. The 0.5.4 version is not build and tested but functionally identical to 0.5.3. 

The design is provided as is. Just as it is stated in the license. The design is a hobby project and not specificly designed to adhere to any standard, so use it at your own risk.

A stand alone Peak and Hold injector driver board is now in a seperate repository. See: https://github.com/Tjeerdie/Peak-And-hold-Driver

## Getting Started
Take a look at the very informative manual for speeduino:
https://speeduino.com/Speeduino_manual.pdf

There is a difference for the TPS with respect to the manual. The TPS must be fed by 3.3V and not 5V like the other speeduino boards. For best performance it is better to wire all the grounds of the sensors to the GND pins and not use the PWR_GND or carchassis for this. 

How to load the firmware to the STM32 see:
https://speeduino.com/forum/viewtopic.php?f=13&t=1914&p=26572#p26572

## Board pinout

The TS Mapping column is the pin you enter in the "Local Auxillary Input Channel Configuration" when repurposing the input pins for another purpose (example: oil pressure sensor):
https://speeduino.com/forum/viewtopic.php?f=14&t=2809

| Pin# | Function   | Alternative | Switch | Tuner Studio Mapping |
|-----|-------------|-------------|--------|------------|
| 1   | GND_PWR     |             |        |            |
| 2   | GND_PWR     |             |        |            |
| 3   | 12V_ECU     |             |        |            |
| 4   | 12V_ECU     |             |        |            |
| 5   | INJ_CH8     |             |        | 66         |
| 6   | INJ_CH7     |             |        | 67         |
| 7   | INJ_CH5     |             |        | 62         |
| 8   | INJ_CH6     |             |        | 64         |
| 9   | IDLE1-OUT   | STEP_1A_OUT | JP5    |            |
| 10  | BARO        |             |        | A13         |
| 11  | Spare_2_out | Step_2B_OUT | JP6    | 71         |
| 12  | Spare_1_Out | Step_1B_OUT | JP7    | 72         |
| 13  | IGN_CH1     |             |        |            |
| 14  | 02_2        |             |        | A4         |
| 15  | FAN         |             |        |            |
| 16  | IDLE2-OUT   | STEP_2A_OUT | JP8    |            |
| 17  | IAT         |             |        |            |
| 18  | IAT_2       |             |        | A0         |
| 19  | FUEL_PUMP   |             |        |            |
| 20  | CLT_2       |             |        | A1         |
| 21  | RS232_TX    |             |        |            |
| 22  | GND         | IGN5-OUT    | JP18   |            |
| 23  | O2          |             |        |            |
| 24  | INJ_CH4     |             |        |            |
| 25  | MAP         |             |        |            |
| 26  | GND         | IGN6-OUT    | JP16   |            |
| 27  | CLT         |             |        |            |
| 28  | INJ_CH3     |             |        |            |
| 29  | CANH        |             |        |            |
| 30  | GND         |             |        |            |
| 31  | IGN_CH2     |             |        |            |
| 32  | INJ_CH1     |             |        |            |
| 33  | GND         |             |        |            |
| 34  | RS232_RX    |             |        |            |
| 35  | TPS         |             |        |            |
| 36  | IGN_CH3     |             |        |  24        |
| 37  | 5V          |             |        |            |
| 38  | FLEX_IN     |             |        |            |
| 39  | VR2-        |             |        |            |
| 40  | IGN_CH4     |             |        |  34        |
| 41  | VR2+        |             |        |            |
| 42  | VR1-        |             |        |            |
| 43  | VR1+        |             |        |            |
| 44  | INJ_CH2     |             |        |            |
| 45  | CANL        |             |        |            |
| 46  | 3.3V        |             |        |            |
| 47  | BOOST-OUT   |             |        |            |
| 48  | TACHO-OUT   |             |        |            |

![connector pinout](/figures/pin_out.png)

## Jumper settings
There are 12 jumpers on the board to set/change various hardware configurations to suit your needs. with a sharp object scratch away the default bridge and use a solder bridge between the alternative configuration pins. The pull up resitors (JP1/JP4) are briged vs non bridged and no need to skratch anything away.
| JP# | Function                  | Default       | Alternative|
|-----|---------------------------|---------------|------------|
| 1   | Halleffect Pullup resistor| Not Conneced  | Connected  |
| 2   | Halleffect or VR input VR1| VR            | Hall       |
| 3   | Halleffect or VR input VR2| Hall          | VR         |
| 4   | Halleffect Pullup resistor| Not Conneced  | Connected  |
| 5   | STEP_1A_out or IDLE1-OUT  | IDLE1-OUT     | STEP_1A_OUT|
| 6   | Spare_2_out or Step_2B_OUT| Spare_2_out   | Step_2B_OUT|
| 7   | Spare_1_Out or Step_1B_OUT| Spare_1_Out   | Step_1B_OUT|
| 8   | IDLE2-OUT or STEP_2A_OUT  | IDLE2-OUT     | STEP_2A_OUT|
| 9  | Tacho out voltage		  | 12V output     | 5V output |
| 10  | Ignition trigger out voltage		  | 5V output     | 12V output |
| 15  | Flex fuel or Boot0 in     | Flexfuel      | Boot0      |
| 16  | Ignition 6 or GND         | GND           | IGN6       |
| 18  | Ignition 5 or GND   _     | GND           | IGN5       |


## Information for assembling a V0.5.X board
Information for board assembly and choosing components. If  you plan to build one of these it is important to note that a little electronic knowledge is very helpful if not essential to get the board working. The accompanying JLC bom list has most passive components in it, but not all components, some self assembly/soldering and part selection is required.  

### RS232 and bluetooth
The hardware serial port 1 is shared between bluetooth and RS232 output on the ECU connector. So that means you can only build it with the bluetooth module in place OR the max232 ic in place not both! That will break the communication. 

Dont forget to configure the bluetooth module to use 115200 bps baudrate using the HC-05/HC-06 AT commands. 

If you want your main/Tuner studio communiation to use the hardware serial port 1 (So bluetooth or RS232 on the ECU connector). Build the speeduino firmware in the arduino IDE with no "usb support" -> "None". In that case it will default to use hardware serial 1 as the communication.

If the bluetooth comms are not working and you are using a HC-05 or HC-06 module (both are 3.3v so its safe to direcly connect to the MCU). For V0.5.2 of SPECTRE [R37,R38] can be replaced by 0 ohms. For V0.5.3 [R38] can be replaced by 0 ohm. 

### Zener diodes
If you build the board with the injector driver mosfets to be BSP78 [Q10,Q11,Q13,Q14,Q18,Q19,Q20,Q21] you can leave the bzx84C39 + 1N4148 out [33,D34,D35,D36,D37,D38,D39,D40,D41,D42,D43,D44,D45,D46,D47,D48]. These are used for clamping, but the BSP78 has internal clamping. You can use other mosfets with SOT223 footprint in place of the BSP78. If these are not clamped or reptetative avalanch rated use the clamping diodes to keep them in spec.

### Vehicle Speed input
Note: This workaroud is no longer working. There is no solution yet.

Here is a scription how to use one of the analog spare inputs (IAT_2 = ECU pin 18) as VSS input for speeduino. This can be a hall type sensor or a porximity sesnsor. it can NOT be a VR type sensor
1. Remove C2 and C4 from the board
2. On the MCU pin headers of the board connect PA0 to PA2 with a bit of solder
3. in Tuner Studio select pin 50 (PA2) for the VSS input pin.

PA0 (pin 48 in TS) can not work as VSS pin because of conflicting interrupts with the crank sensor (PE0)


## Tested on V0.5.2/V0.5.3
The following functions have been tested and confirmed to be working on a volvo B230FK redblock engine. This a 4 cylinder engine with small turbo. A VAG wasted spark coil with internal drivers is used as ignition<br/> 

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
BOOST output [OK]<br/>
Stepper idle output [OK]<br/> 
TACHO out [OK]<br/>

## To be tested on V0.5.2/V0.5.3
BARO <br/>
CAN bus TX<br/>
CAN bus RX<br/>
FLEX fuel input<br/>
Coolant temperature (CLT_2) <br/>
Inlet Air Temperature (IAT_2) <br/>
Lambda sensor (O2_2) <br/>

## License
This project is licensed under the GNU GENERAL PUBLIC LICENSE - see the [LICENSE.md](LICENSE.md) file for details


