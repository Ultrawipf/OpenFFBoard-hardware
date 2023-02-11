## BISS-C module

This module allows the OpenFFBoard to use its SPI3 (EXT) header to communicate with common BISS-C encoders like the JKD-4-22PF-G05BL (used on Mige motors).

The SUB-D 15 female connector matches the pinout of Mige motors and some others directly.

The CS pin connection is optional. When left disconnected or low the transceivers are active, when high the transceivers are off.

The BISS-C encoder module can only be used with certain motor driver modes:

-   TMC via forwarding

-   VESC as secondary encoder

-   PWM


