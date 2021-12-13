## INA333 3-wire Loadcell amplifier

Connections:
###
- Vin   :   3.3V/5V supply and load cell positive
- GND   :   GND and load cell negative
- IN    :   Load cell center/signal
- OUT   :   Amplified signal. Connect to ADC input

Gain setting: 10-1000, Clockwise rotation to increase
Offset: Clockwise to move the output up, ccw to move the output down to GND

Retune the offset when changing the gain and carefully check the output voltage to get the offset perfect.

The CPL and BOM files contain LCSC part numbers and be used on [JLCPCB](jlcpcb.com/). 
