# 8-DI-ESP32-PCB
A printed circuit board that enables a ESP32 to interface with digital inputs up to 28VDC.

# Features
- 8 Galvanically isolated inputs
- Pluggable terminal blocks for connecting sensors
- Supports 12 and 24VDC sensors
- ESD protected inputs
- Reverse polarity protection
- Over current protection

# Technical Specification
- ESP32 Input voltage 5-16VDC
- Sensor Input voltage 5-28VDC (with 3/4W input resistors)
- Maximum input current draw 12mA
- Maximum board power draw ~10W

# Schematic
![Schematic](/Schematic.png)  

# How to use
- J9: Screw terminal for supplying voltage to the sensors that are connected to the optocouplers. Input voltage range: 5-24VDC
- J10: Screw terminal for supplying voltage to the ESP itself. Input voltage range: 5-12VDC

- D11: Led to indicate the presents/absent of a voltage on the VCC rail (J9).
- D12: Led to indicate the presents/absent of the +3V3 rail (J10).

- JP1: Jumper to connect the VCC to VPP. Used to remove the Galvanic isolation between the sensors and ESP.  
**Only populate this jumper if one voltage source is being used!**
- JP2: Jumper to connect GND1 to GND2. Used to remove the Galvanic isolation between the sensors and ESP.

- J1-J8: Each digital input has its own header connected to the ESP. Pinout from left to right: 1=VCC, 2=GND and 3=GPIO

- SW1: Resart the ESP
- SW2: put the ESP in program mode if the ESP is booting

- J11: Program connector. Connect any +3V3 UART programmer to write a program to the ESP.  
note: the ESP needs to be manualy set to program mode via SW1 and SW2.

# I/O mapping:  
- J1 -> GPIO36
- J2 -> GPIO39
- J3 -> GPIO34
- J4 -> GPIO35
- J5 -> GPIO19
- J6 -> GPIO21
- J7 -> GPIO22
- J8 -> GPIO23
