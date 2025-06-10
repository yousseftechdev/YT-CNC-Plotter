---
title: "YT CNC Plotter"
author: "Youssef Tech"
description: "A mini CNC Plotter to trace PCB designs on copper plates"
created_at: "2025-06-09"
---

Total time spent: 13 hours and 25 minutes
Total cost of parts (as of the time of writing this line and without 3D printing): 1,456.75 EGP or 29.37 USD
Approx. 3D printing cost: 315 EGP or 6.35 USD

# [2025-06-09] [Time spent: 6 hours] Day 1: Brainstorming, and first steps
I'm trying to imagine how this thing would work, I was thinking of belt drives at first, but then i felt that it wouldn't be very accurate.

For now I'm making a list of the components I'll be using.

So I found a similar project online that I'll be taking inspiration from for this project, and it utilizes the following components

The list:
- Arduino Nano for control
- 3x Stepper motors (Model: 28BYJ-48)
- 3x Stepper motor drivers (Model: ULN2003)
- 3D printed frame

These are the main components at least, I didn't think of the other small components I'll need, like capacitors and stuff

Started designing the PCB in KiCad, and making a BOM as I go.

Finished PCB design, FINALLY. The pcb took HOURS to finish, made me wish I had gone with the breadboard method instead. Hoping it works when I actually order it 😭🙏🏻

PCB Images:
Schematic:<br>
![shematic](imgs/Schematic.png)

PCB Design:<br>
![design](imgs/PCB-2D.png)

PCB Model:<br>
![model](imgs/PCB-3D.png)

# [2025-06-10] [Time spent: 7 hours and 25 minutes] Day 2: 3D modeling
It's 6:35 AM as of writing this, I haven't slept yet since finishing the PCB (started Day one at 10 PM yesterday, finished at 4:45 AM). I've decided to start working on the 3D models I'll need for this project, idk anything about CAD and idk how I'm gonna get the motors to move the pointer/pen correctly, so I'm gonna start by making a case for the control board I designed yesterday.

The program I've decided to use is Fusion 360, no specific reason why I chose it. Currently watching a tutorial on how to use it since it's my first time in a CAD software.

Took some measurements from the PCB in KiCad so I can make the case as much of a tight fit as I can.

Put some mounting holes in the PCB and put some pegs in the case for the PCB to mount onto.

Man I didn't realize Fusion was such a pain 😫, all the YouTubers made it seem like the best CAD software ever or sum.

CREATED A CUBE 🔥🔥🔥<br>
HOLLOWED THE CUBE 🔥🔥🔥

I left a 1 mm clearance between the case walls and the and the PCB itself, and made a lid.

Added opening for motor cables (Almost forgot that)

Finally done with the case, can't beleive I spent that much time on this case, it is now 7:57 AM, almost one and a half hours on this:<br>
![case](imgs/PCB-Case.png)

Aaaand now for the task I've been putting off since the start... the FRAME 💀!!!

Idk how to get started on this tbh, but I'll try, maybe I look at similar projects to get an idea about how they get the gear teeth number and all those details.

After looking at multiple projects I noticed that most of them used a 9 tooth gear to drive the axis, so I guess I'll be using the same number.

HOW DO I CREATE A GEAR in Fusion!!?!?!

Starting to get sick of tutorials here<br>
![tutorial](imgs/gearTutorial.png)

Ok I'm getting there but I'm trying to figure out how to get the shape of the hole in the gear to be like the shape of the shaft of the motor, the gear looks like this for now:<br>
![gear](imgs/gear.png)

And this is what the shaft shape looks like, it's called a "Double D" shape:<br>
![shaft](imgs/shaftShape.png)

FINALLY GOT IT, after lots of tutorials, I finally got the gear right:<br>
![final-gear](imgs/finalGear.png)

Now comes the easy part, the rails, since I already know the gear's properties I can just use the same ones on the rail/track and they'd mesh together perfectly.

This is the base track, it has mounting holes and a place to mount the motor with the gear attached to it:<br>
![base](imgs/base.png)

And this is the primary gear track, it meshes with the gear on the motor mounted to the base to control the Y-Axis, it also has a platform to mount the X-Axis base onto it:<br>
![track1](imgs/track1.png)

Half the work is now done, the next few parts are going to be easier to model since they're just slightly modified versions of the previous parts.

The X-Axis base is now FINISHED, YIPPEE, it will be mounted on the primary track and will be used to hold the secondary track which will move the Z-Axis motor AKA the Pen motor:<br>
![base2](imgs/base2.png)

The secondary track is basically the primary track but with a motor mount instead of the base mount:<br>
![track2](imgs/track2.png)

This pretty much concludes the main stuff, like these could somewhat work on their own, but there are some finishing touches I wanted to add.

If you haven't noticed at the end of the X-Axis base there are mounting holes for something, they're for a roller/wheel, it acts as a stand to reduce friction between the X-Axis base and the Y-Axis base, and prevents friction with the surface the CNC Plotter is mounted on by having a rolling wheel, it consists of two parts, the wheel itself and its holder:
- Holder:<br>
![holder](imgs/holder.png)

- Wheel:<br>
![wheel](imgs/wheel.png)

Now, all that's left is the Pen holder, it's a combination of two hollow cylinders connected by a rectangle, one of the cylinders has the Double D hole cutout to make it fit onto the Z-Axis motor, I've design multiple different sizes so it can fit all pens/pencils:
![penholder](imgs/penholder.png)

After the parts arrive and the frame gets printed I'll get the chance to write the firmware for this project.
