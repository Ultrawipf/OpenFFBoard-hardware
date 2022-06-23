# Shift register button module

This module allows the connection of up to 32 (or more if chained) buttons to any spi capable microcontroller or as a button source in the OpenFFBoard firmware.


### Connections
* V+ - 3,3V (or 5V)
* OUT - MISO of controller
* CS (Latch) - CS pin of controller
* CLK - SCK
* GND - GND

* IN - OUT of previous module
* Buttons between GND and any input pin


### Configuration in OpenFFBoard

Select SPI button source, select 74HC165 mode and invert buttons and the amount of used buttons (up to 32 for 1, up to 64 for 2 modules)