# OpenFFBoard-hardware
This contains the hardware designs of the OpenFFBoard

These are work in progress.
No guarantee for functionality or safety! The designs are NOT FINALLY TESTED.
The firmware is available in the main [OpenFFBoard](https://github.com/Ultrawipf/OpenFFBoard) git.

This project requires soldering of many fine pitched parts.

Full Kits will be available later once everything is tested. Check the [Discord](https://discord.com/invite/gHtnEcP) and [project page](https://hackaday.io/project/163904-open-ffboard) for updates.

Changelog:
### TMC Driver:

##### 1.1: (Prerelease prototype)
- Added filtering for Hall and Encoder inputs.
- Separated TMC and STM VM sense dividers

##### 1.2: (Major redesign)
- Using TMC4671-LA production version
- Added 5V buck converter
- Added emergency shutdown method by pulling enable low
- Rotated power stage. Moved all motor connectors to one side
- Moved analog encoder pins and routed differential inputs out
- Improved vcore impedance
- Increased encoder filter frequencies
- Reduced resistance of sense dividers
- Switched LM5050 to LM74700
- Space for 2 VM capacitors
- Improved mosfet protection
- Added temperature sensor pads on AGPI-B
- 50x50+100mm screw holes

### STM USB Interface:
##### 1.1.1:
- Renaming some pins
- Added FFBoard logo
- Changed USB diode to SMC
Added zener pad on 5V
Removed encoder buffer
Higher value pwr led resistor
Added pads for SW
Minor routing changes
