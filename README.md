# Meteoroid
<img src="https://raw.githubusercontent.com/techy-robot/Meteoroid/refs/heads/main/Media/Logo/Meteoroid-logo.svg" width="100">

Production-ready 3d printer based on a Ender 5 frame, with multifunction tool changing, bed changing, and accessories with robots.

Preview Picture
![](https://raw.githubusercontent.com/techy-robot/Meteoroid/refs/heads/main/Media/Screenshot%20from%202025-04-05%2022-23-54.png)

V0.5 [Onshape Link](https://cad.onshape.com/documents/1de0655c0501c319c0be82e5/v/822dbc763cf3844d6902b3b4/e/f03e8779d1a8cc2741025c01)

It is desktop machine with plug and play heads. Chain these machines together and add robot carriages in between and you got yourself an awesome modular factory that can fit on a bench. The cost of the _entire system_ will likely be several thousand dollars, with the main machine between $300 to $500. I aim to lower the cost of a complete industrial system as much as possible.

The base machine is a CoreXY printer with a 500+mm/s move speed 30k+ accel, and 4 tool changer slots. The printer can be partially enclosed, with openings for robots to quick swap tools and beds and sometimes even sub-tools (Like a PnP head with different nozzle sizes). Software-wise, it will be running Klipper, which can interface with other software like OpenPNP using macros and linux ports.

Features:
- Standard 235mm x 235mm heated bed size with Garolyte bed for easy print release, supported by dual z-axis motors to provide stabilty without the complexity of an automatic leveling trimotor bed.
- Klipper
- Tool changer with 4 slots
- CoreXY
- Medium cost desktop production system
- Completely Open-Source
- 3 Accessory slots for extra toolhead elements like PnP heads or a camera
- Off-the-shelf components that are well known and high-quality, with many parts 3D printed in ASA
- Optional enclosure
- High print speed 500mm/s and 30k accel


I designed a little adapter board I called Klipper to CACKLE. It basically takes USB-c input and 24v power, and converts this to my CACKLE layout spec and RS485 communication protocal. It uses a CH32 chip to process the commands and output equivalent Luos spec datapackets over the bus to my system.
![](https://raw.githubusercontent.com/techy-robot/Meteoroid/refs/heads/main/Media/Screenshot%20from%202025-04-06%2000-21-57.png)

# Building
I don't have specific build instructions yet as that takes a lot more development time, but you can reference the [BOM](https://github.com/techy-robot/Meteoroid/blob/main/BOM_Main%20assembly_simplified.csv) and the CAD file/Onshape to get all the parts and build it.

# Development Log
Total Hours Spent designing: 51 hrs

This project was worked on sporadically from Feb 1, 2025 to April 5th, 2025

See [Changelong](https://github.com/techy-robot/Meteoroid/blob/main/Changelong.md) for my full development log and the nitty-gritty details

# Credits
The motion system inspiration is from [Zero G Mercury 1.1](https://docs.zerog.one/manual/build/mercury_eva), which is a relatively simple corexy conversion for ender 5-style frames. I have tweaked many of the parts to fix small issues I noticed, revamped the frame with supports, added a toolchanging solution, and a 2 axis bed leveling system instead of the more costly 3-axis Hydra solution. The toolchanger is similar to the [Daksh V2](https://github.com/ankurv2k6/daksh-toolchanger-v2/) solution, except with a simpler single lock system, and concentric kinematic mount points instead of asymetrical contact mounts.

Everything else should be my own design, from the upcoming bed changing solution, upcoming robotic arms, toolheads, and the asteroid texture used on some of the parts.