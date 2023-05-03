# CG Proto 2 Wiring Guide

## Assembling the PCB

The PCB assembly should be pretty straightforward. It is simply a breakout board for many of the ESP32’s connections.

You will need fifteen three-pin male dupont connectors, two fifteen-pin female dupont connectors, one 2x4-pin female dupont connector, a 1000uF capacitor, a 680ohm resistor, and a four-pin male dupont connector with the second and fourth pins cut off.


## Wiring the finger modules

You can get started on wiring up your potentiometers once you’ve reached this stage of printing and assembly.

<p align="center">
<img src="/guides/images/wiring/wiring_requirements.png" height="300">
</p>


**Figure 1: Tools required for finger module wiring**

For each hand, you’ll need ten three-pin dupont connectors, a length of ribbon cable (I like to use salvaged IDE cables), a crimping tool, and a soldering kit.

Cut twenty three-pin cables to the lengths found in Table 1. Crimp them with three pin female dupont connectors.

<p align="center">
<img src="/guides/images/wiring/cut_and_crimped_cables.png" height="300">
</p>


**Figure 2: Cables cut to length**

**Table 1: Rotation of spools and length of cable**

| Finger | Spool Rotation | Curl Cable Length | Splay Cable Length |
|:-----------------:|:--------------------:|:---------------------:|:----------------------:|
| Right Thumb | Clockwise | 8” | 8” |
| Right Pointer | Counterclockwise | 7” | 7” |
| Right Middle | Counterclockwise | 6” | 6” |
| Right Ring | Clockwise | 5” | 5” |
| Right Pinky | Clockwise | 6” | 6” |
| Left Thumb | Counterclockwise | 8” | 8” |
| Left Pointer | Clockwise | 8” | 8” |
| Left Middle | Clockwise | 6” | 6” |
| Left Ring | Counterclockwise | 5” | 6” |
| Left Pinky | Counterclockwise | 5” | 6” |

You will have to cross one of the wires, since the middle pin of the breakout PCB is the VCC pin and the middle pin of the potentiometer is the signal pin. The recommended pinout of the cables is shown below.

<p align="center">
<img src="/guides/images/wiring/soldering_diagram.png" height="300">
</p>

**Figure 3: Soldering guide for module cables**

On the left hand, the pair of wires farthest from your wrist should be crossed, and on the right, the pair of wires closest to your wrist should be crossed. This ensures a consistent pinout across the entire pair, and will make it easier to configure in software later. Both the curl and splay potentiometers should be soldered this way. (Because the spin direction of the potentiometers is reversed on the pointer and middle finger, the firmware will need to be configured to reverse the measured value later)

My technique is this: Tin the ends of the wire, then heavily tin the end of the potentiometer. Use a helping hand to hold the module, then with your hands, hold the wires and soldering iron. Solder each wire one at a time, and give the module a chance to cool down between each pin soldering to prevent burning out the potentiometer.

When you are finished, you’ll have something that looks like this:

<p align="center">
<img src="/guides/images/wiring/connected_loose_cables.jpg" height="300">
</p>

**Figure 4: Soldered finger modules with un-managed cables**

Organizing the wires is a little… chaotic. I usually just try to corral them together as much as possible towards the pinky, plug ‘em in, then try to zip tie them in place. I’m still working on the cable lengths and am hoping to add more cable channels and perhaps update the PCB to alternate curl/splay to reduce the amount of weird overlap we have.

But, when you’re finished, you should have something that looks like this:

<p align="center">
<img src="/guides/images/wiring/final_product_cropped.png" height="300">
</p>


**Figure 5: Completed Finger Tracking Module**


## Calibrating and Installing the Servos

TODO

