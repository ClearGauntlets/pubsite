# ClearGauntlet - Joystick PCB
Joystick PCB - Schematics Design for interfacing between Joycon's joystick and main PCB.

**Motivation**: We are using a thirdd party joystick such as [here](https://www.amazon.com/BRHE-Switch-Joystick-Replacement-Controller/dp/B097QPKRR8/ref=sr_1_5?crid=2JRAXLZX0SBR4&keywords=joycon%2Bjoystick%2Breplacement&qid=1675712249&s=electronics&sprefix=Joycon%2Brep%2Celectronics%2C78&sr=1-5&th=1). Since the flex cable is very short and flimsy, we want to create a small PCB board to hold, and connect pins to the main PCB more reliably. 

## Components
### Joystick
This joystick is the 3rd party replacement for the joycon. 
![613xcOPRD7L _AC_SL1500_](https://user-images.githubusercontent.com/44926107/219124705-d384329b-2a31-4060-84aa-e52712121337.jpg)

**Schematics**
The measurement of the joystick in mm:
![168402839-7e5a9171-2141-463a-acbf-c453b9bc75b0](https://user-images.githubusercontent.com/44926107/218548176-4535d6ac-1be7-4794-b494-146a075ac5a7.png)


## Adaptor
We need a 5-pin (0.5mm spaced) adaptor to connect on the board and split the pins to the standard dupont spacing (2.56 mm).

This model can be found on Mouser.

![molex-5pin](https://user-images.githubusercontent.com/44926107/219127868-a6d7fc4d-767e-4130-a259-df0db0de7329.png)


## PCB

3D model
![joycon-pcb-3](https://user-images.githubusercontent.com/44926107/219124693-14d1507d-82b4-4552-9cc6-0f68ae957be0.png)


## Assembly
The joystick will be mounted on the backside of the PCB either by through holes or hot glued it directly. Then, the flex cable will connect to the adaptor. A horizontal 5-pin male dupont will be place at the J2 and run a wire to the main PCB.  The idea is to make PCB-joystick as a module which will be placed on the side of the index finger.