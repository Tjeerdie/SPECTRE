# Project SPECTRE
Project SPECTRE	(Speeduino PrintEd Circuit TjeeRdiE). This is a board with the hardware to run speeduino on a STM32F407VE6T board from ebay. (Or a STM32 BLACK_F407VE as i call it). Schematics and more information on the cpu board can be found here: [Link] (https://github.com/mcauser/BLACK_F407VE) 
BLACK_F407VE. This is a design in Kicad so to open the files use Kicad. The intension of the board is to use minimal hardware next to the board and casing. So injector voltage, MAP power IGN power etc are all available from the connector directly. For a 4 cylinder NA engine with wasted spark and full seqential injection you would only need a relay for the fule pump and a relay for the FAN if needed. The board fits inside the ebay ECU housing with 48pin connector.

## Getting Started
Well there is no getting started because this board is not fully tested and debugged yet. Current status of design mistakes and fixes for version 0.4 can be found in [TODOFixes](TODOFixes). The intension is to get a version 0.4 fully working board out as soon as time permits.

## Tested
The following functions have been tested en confirmed to be working with real car hardware and provide good results.<br/> 
Halleffect trigger input (Trigger 1) [OK]<br/>
Halleffect trigger input (Trigger 2) [OK]<br/>
Inlet Air Temperature (IAT) [OK]<br/>
Manifold Absolute pressure [OK]<br/>
Injector outputs [OK]<br/>

## Tested and working with modifcations
Coolant temperature (CLT) [OK]<br/>
PWM idle output [OK]<br/>

## To be tested
Stepper idle output<br/> 
Ignition outputs <br/>

## License
This project is licensed under the GNU GENERAL PUBLIC LICENSE - see the [LICENSE.md](LICENSE.md) file for details


