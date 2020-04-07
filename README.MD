# Project SPECTRE
Project SPECTRE	(Speeduino PrintEd Circuit board TjeeRdiE). This is a PCB with the hardware to run speeduino on a STM32F407VE6T daugther board from ebay. (Or a STM32 BLACK_F407VE as it is sometimes called). Schematics and more information on the cpu board can be found here: (https://github.com/mcauser/BLACK_F407VE) 

This is a design in Kicad so to open the files use Kicad. The intension of the V0.3 board is to use minimal hardware next to the board and casing. So fused injector voltage, MAP power IGN power etc are all available from the connector directly. For a 4 cylinder NA engine with wasted spark and full seqential fuel injection you would only need a relay for the fuel pump and a relay for the cooling Fan if needed. The board with daugther board fits inside the ebay ECU housing with 48pin connector.

From version V0.4 and on the idea is to use more pins for other functions. like CAN bus and RS232 more ignition/injection outputs. So now a fuse and relay box need to be used to connect it to the car. 

From version V0.5 and onwards 4/8 injector outputs are designed for PWM peak and hold drivers. This is usefull for low-z injectors. The idea is to use 4 drivers for petrol injection normal saturated mode and 4 drivers for LPG vapour injection with a second fuel table. LPG vapour injectors are normally low-z (between 2.5 to 4 Ohm). The necessary changes in speeduino software are not developed yet. No worries until that time it will work as normal injector drivers. 

A LTspice simulation of PWM peak and hold drivers is also in the LTspice folder. It is nice to see the wave forms used and the current thru the coil.

##Photos
Check out the SPECTRE_V0.3\photos folder to see the real thing! For version V0.5 there are some 3d renders in the folder.

## Getting Started
Well there is no getting started because this board is not fully tested and debugged yet. Current status of design mistakes and fixes for V0.4 and V0.5 can be found in TODOfixes file. The intention is to test V0.3 fully before getting a version V0.5 or V0.6 board out on the bench. 

## Tested on V0.3
The following functions have been tested and confirmed to be working with real under the bonnet hardware and provide good results.<br/> 
VR1 input (Trigger 1) [OK] <br/> 
VR2 input (Trigger 2) [OK]<br/> 
Halleffect trigger input (Trigger 1) [OK]<br/>
Halleffect trigger input (Trigger 2) [OK]<br/>
Inlet Air Temperature (IAT) [OK]<br/>
Manifold Absolute pressure [OK]<br/>
Injector outputs [OK]<br/>
Lambda sensor (O2) [OK]<br/>
Throttle position input [OK]<br/>
Bluetooth module (PD8,PD9) [OK]<br/>

## Tested and working with modifcations
Coolant temperature (CLT) [OK]<br/>
PWM idle output [OK]<br/>

## To be tested
Stepper idle output<br/> 
Ignition outputs <br/>
Fuel pump relay <br/>
FAN relay <br/>
BARO <br/>
FLEX fuel <br/>
Coolant temperature (CLT_2) <br/>
Inlet Air Temperature (IAT_2) <br/>
Lambda sensor (O2_2) <br/>
TACHO out <br/>

## License
This project is licensed under the GNU GENERAL PUBLIC LICENSE - see the [LICENSE.md](LICENSE.md) file for details


