# YT CNC Plotter
This is a hobby project, it's basically a Mini CNC Plotter made using small 5v stepper motors and an Arduino Nano, I'll use it to draw circuits on copper plates to essentially make DIY single layer PCBs.

## How does it work?
It uses gear tracks the are moved by the stepper motors, two stepper motors are used to control the X and Y position of the pen and the third motor is used to control the Z position aka the up and down movement of the pen, a script will be used to translate normal G-Code that's used in big CNC machines into something the Arduino can understand.

## Parts??
Most of the electronics are going to be soldered onto the PCB except for the motors, as for the mechanical parts they're 100% 3D printed, no need for anything more than screws to put everything together

Electronics:
- Arduino Nano to control the motors
- 3x 28BYJ-48 Stepper motors
- 2x ULN2003A motor driver (Transistor arrays)
- 2x 100 nF capacitors
- 100 uF capacitor
- Barrel Jack
- 3x JST HX Ports for motors
- LED (OPTIONAL)
- 220ohm resistor (OPTIONAL)

## What have I learned?
I have learned so much about CAD from making this project, this has been such a great learning experience, but the most important thing I've learned is not to use Fusion 360 ever again.