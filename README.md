# OpenFFBoard-hardware
This contains the hardware designs of the OpenFFBoard

These are work in progress.
No guarantee for functionality or safety! The designs are experimental and may change at any time.
The firmware is available in the main [OpenFFBoard](https://github.com/Ultrawipf/OpenFFBoard) git.

This project requires soldering of many fine pitched parts including QFN. Availability of components may change over time so check for alternatives if something is not available.
The motor driver should be made with 2oz copper layers for best thermal performance!

The firmware may run on some third party development kits but as they have different pinouts and missing peripherals this is not recommended.


If you don't want to solder yourself full Kits may be available in small batches on [Elecrow](https://www.elecrow.com/open-ffboard-stm32f407-usb-interface-only.html), [Tindie](https://www.tindie.com/stores/gigawipf/) or Discord.

Check the [Discord](https://discord.com/invite/gHtnEcP) and [project page](https://hackaday.io/project/163904-open-ffboard) for updates.


### LICENSE NOTE: The root license applies to all subfolders NOT containing their own LICENSE file. If a subfolder contains a different LICENSE file this different license applies to all subfolders below this LICENSE file.

**If you want to sell any hardware of this project yourself i would kindly ask you to get in contact with me ([mail](mailto:ffboard@y-richter.de) or Discord)**

Changelog:
### TMC Driver:

#### 1.1: (Prerelease prototype)
- Added filtering for Hall and Encoder inputs.
- Separated TMC and STM VM sense dividers

#### 1.2: (Major redesign)
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

#### 1.2 fix:
- Fixed silkscreen (R18 and R19 swapped)
- Modified some labels
- Added 33k gate pulldown for brake resistor
- Moved and resized vias in motor driver part (Manufacturing reliability)
- Tented vias

#### 1.2.2 (HALL):
- Redesigned power stage to use hall sensors (LEM GO SME and TMCS1100)
- Changed buffers to 74LV17APWJ
- Added opamp for TMC inputs (temperature and voltage sensing)
- Used opamp as comparator for hardware brake resistor activation point (~65V)
  
### 1.3.3:
- Analog section with separate LDO
- Support for more current sensors (ACS724)
- Optimized gate driver circuit w. resistors and diodes
- More separation between analog and power sections

### STM USB Interface:
#### 1.1:
- Initial prototype
- STM32F411RE based
- Only supports TMC4671 driver
- Only one SPI2 CS

#### 1.2:
- STM32F407VG
- Reserved PWM pins
- 3 CS pins per SPI
- CAN bus
- Reserved E-Stop
- USB Vbus sense
- separated ADCs for vsense and analog in
- LEDs moved
- Added FFBoard logo
- Changed USB diode to SMC
- Added zener pad on 5V
- Removed encoder buffer
- Higher value pwr led resistor

#### 1.2.1:
- Fixed some labels
- Moved USB socket and terminals slightly to the corners (Big usb plugs might interfere with the pins)
- Changed crystal load capacitors to lower values. (F407 DFU is very sensitive and does not work reliably with too high value caps)
- Added E-Stop capacitor against noise triggering it
- Tented vias

#### 1.2.2
- Swapped (Previously unused) Encoder Z pin from pin 65 to pin 62 because of interrupt conflicts with the DRV flag pin

#### 1.2.3
- USB-C instead of micro USB
- SPI1 uses a 2 row header
- Additional USB protections

#### 1.2.4
- Moved EXT header slightly
- Used 2 extra jumper pins for CAN termination instead of solderjumper
