# ClearGauntlet-PCB-rev B
PCB - Schematics Design for VR Gloves

A breakout board for ClearGauntlets, aimed at improving cable management and minifying electronics of VR Gloves.
<!-- https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax#hiding-content-with-comments -->


![cleargauntlet-revb-rtx-on](https://user-images.githubusercontent.com/44926107/216163901-b83deb26-56f4-4fab-bbbe-1541b22418f5.png)

## Specs
The board has the following I/O:

- 1 ESP 32 V1
- 10 potentiometers, each requires 1 3.3V pin, 1 GND, 1 Analog pin.
- 5 servo motors, each requires 1 5V pin, 1 GND, 1 Analog pin.
- 2 pushed bottons
- 1 joystick (5 pins)
- 1 power JST connection (3 pins: 1 5V and 2 GND)

## Pin details

![revB-schematics](https://user-images.githubusercontent.com/44926107/217057736-99c32545-b9b3-4773-8112-eaac8b957907.png)

## Assembly
To assemble the board, you'll need
- 30 pins Female Dupont Connectors, 2.54mm pitch (2x 15-pin). This is for holding the ESP-32
- 15 x 3 pins Male Dupont Connectors, 2.54mm pitch, for connecting potentiomers, servos)
- 2 x 2 pin Male Dupont for push buttons and 5 pin Male Dupont for Joystick
- 1 ESP32

It's all just through-hole soldering, so it goes pretty quick once you have the parts. Use the CAD renders as a guide.

You will also probably want to create a 2-pin 5V USB cable like this one:

![IMG_1019](https://user-images.githubusercontent.com/42927786/213874292-f878529d-52b0-481f-8072-50417f089595.jpg)

It's just power, and ground, and goes into the 5V/GND JST connector next to the ESP32.

**You'll also need to bodge that 5V in pin to the Vin pin that goes to the ESP32**
