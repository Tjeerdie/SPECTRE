# Project SPECTRE
Project SPECTRE	(Speeduino PrintEd Circuit board TjeeRdiE). This is a PCB with the hardware to run speeduino on a STM32F407VE6T board from ebay. (Or a STM32 BLACK_F407VE as it is sometimes called). Schematics and more information on the cpu board can be found here: (https://github.com/mcauser/BLACK_F407VE) 

Latest version is 0.5.1. Lateste tested version is 0.5. 

A stand alone Peak and Hold injector driver board is now seperate. See: https://github.com/Tjeerdie/Peak-And-hold-Driver

## Getting Started
Well there is no getting started because this board is not fully tested and debugged yet. Version 0.5 is now tested on a real engine and this works as expected! Version 0.5.1 is now in production but there should not be any major issues.

## Tested on V0.5
The following functions have been tested and confirmed to be working with real under the bonnet hardware and provide good results. An 4 cylinder engine with wasted spark is running on this hardware<br/> 

VR1 input (Trigger 1) [OK] <br/> 
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

## To be tested on V0.5
VR2 input (Trigger 2)<br/> 
Halleffect trigger input (Trigger 1)<br/>
Halleffect trigger input (Trigger 2)<br/>
TACHO out<br/>
BOOST output<br/>
Stepper idle output<br/> 
BARO <br/>
CAN bus TX<br/>
CAN bus RX<br/>
RS232 TX<br/>
RS232 RX<br/>
FLEX fuel input<br/>
Coolant temperature (CLT_2) <br/>
Inlet Air Temperature (IAT_2) <br/>
Lambda sensor (O2_2) <br/>

## License
This project is licensed under the GNU GENERAL PUBLIC LICENSE - see the [LICENSE.md](LICENSE.md) file for details


