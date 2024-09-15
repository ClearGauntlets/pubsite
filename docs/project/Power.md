## Power Draw
The motors drain between 0.5 to 1 Amps each.
The ESP32 drains about 0.7 Amps with the IO peripherals connected to 5 motors.

## Wires and Connectors
We used 20 and 22 AWG wires with Dupont connectors for servo motors and potentiometers. For the power supply, we initially used a Dupont connector to a JST connector to the power module to mitigate the chance of the power supply disconnecting.
Note: During Testing, the JST connector melted a bit on the 5V rail. This is due to the amount of current (About 2.7 Amps) running through the wire.
The final connector that ended up being used was a XT30 connector which could handle the current going through the wires. It supported the 4 Amps that the motors were drawing.
