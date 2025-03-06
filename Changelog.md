Made by: @techy-robot

Repository link: https://github.com/techy-robot/Meteoroid

Total hours so far: 8.0 hrs

- [x] I have a 3D printer or will be getting one before March 21st

# Overview
Production-ready 3d printer based on a Ender 5 frame, with multifunction tool changing, bed changing, and accessories with robots.
https://github.com/techy-robot/Meteoroid

It is desktop machine with plug and play heads and beds. Chain these machines together and add robot carriages in between and you got yourself an awesome modular factory that can fit on a bench. The cost of the _entire system_ will likely be several thousand dollars, with the main machine between $300 to $500. I aim to lower the cost of a complete industrial system as much as possible.

The base machine is a CoreXY printer with a 500+mm/s move speed 30k+ accel, and 4 tool changer slots. The printer is partially enclosed, with several openings for robots to quick swap tools and beds and sometimes even sub-tools (Like a pnp head with different nozzle sizes). Software-wise, it will be running Klipper on a RPI zero 2w, which can interface with other software like OpenPNP using macros and linux ports.

Goals/Requirements:
- Standard 235mm x 235mm heated bed size with Garolyte bed for easy print release, supported by dual z-axis motors to provide stabilty without the complexity of an automatic leveling trimotor bed.
- Klipper
- Tool changer with 4 slots
- CoreXY
- Medium cost for a desktop production system
- Completely Open-Source
- 3 Accessory slots for extra toolhead elements like PnP heads or a camera
- Off-the-shelf components that are well known and high-quality, with many parts 3D printed in ABS
- Enclosed
- High speed 500mm/s and 30k accel
- High Quality

Project Time Span: Feb 1, 2025-Present

# Log
This is a log of every day I have worked on this project

## Base Frame - March 5th, 2025

Finished base Frame today, I just need to add stiffeners
![Base Frame](https://raw.githubusercontent.com/techy-robot/Meteoroid/refs/heads/main/Media/Screenshot%20from%202025-03-05%2022-28-12.png)

[Onshape Link](https://cad.onshape.com/documents/1de0655c0501c319c0be82e5/w/00a76129439a8316e13df1dd/m/cbfba813138ca8a3b26123b0/e/76ac3e39a1abc7fd322101c5)

Time: 30 min

## Logo ideas - March 1st, 2025
Some logo ideas
![](https://raw.githubusercontent.com/techy-robot/Meteoroid/refs/heads/main/Media/20250305-logo%20ideas.jpg)

Time : 30min

## Back at it - Feb 25, 2025
Okay, I'm back at it today, starting actual design work! I took my time creating a configerable vslot beam part that can change to any length on demand. I also assembled the base rectangle for the bottom.
![base square](https://raw.githubusercontent.com/techy-robot/Meteoroid/refs/heads/main/Media/Screenshot%20from%202025-02-25%2022-06-22.png)

[Onshape Link](https://cad.onshape.com/documents/1de0655c0501c319c0be82e5/w/00a76129439a8316e13df1dd/m/b323f8763260d1f753c2db33/e/71c7bdc91eebbb5c66aa9fbc)

Time: 1 hr

## More ideas - Feb 4th, 2025

I decided that for rails I should instead go with West3D Berserker MGN12 rails, they high quality and from my favorite supplier

I had a greate idea for a bed ejection and combo scraper system for my printer using one motor. Basically it is a belt drive that at one end pulls the scrapper across the bed towards the front, but if it reverses it disengages and springs back, starting to push the bed out towards the back. There would be a robot port at the back to handle the bed and transport it to storage somehow.

Bed Options:
- 3d Printer bed, G10
- Laser bed with metal heat fins
- CNC Steel bed
- Pick & Place bed with a camera and part alignment jigs

There are also additional slots for toolhead accessories around the top of the printer that would have to be swapped automatically. I'm not sure the best way to replace accessory bays with an automated robot, since its difficult to reach inside the printer. 

Accessory bay options:
- Nozzles for PnP head
- Feeders for PnP
- Klicky Probe
- Waste Material Ejection for color change and cleaning
- Revo hotends
- Camera mount

For the toolhead there are 4 slots for different *active* heads, but many more toolheads will likely be used, and I want them automatically loaded by some robot from storage. I'm thinking of having an extension arm that locks and grabs the toolheads the same way the printer carraige would (in towards the printer), but it would then drop down, go under the frame beam, and be encapsulated into a driving robot to take it to storage.

These robots would be completely independent of the manufacturing machines, they are driving robots with mechanum or swerve base capabily of transporting parts to storage or between machines easily. These carry Heads, Beds, Accessory Bays, Input Material, Output Material, and whatever else I decide should be automatically changed on the fly.

The head and bed should have 2 communication lanes and 2 high power lanes to have maximum flexiblity (if I wanted cameras on the parts for example). It is assumed that CAN bus and or USB 3 are used for high reliability.

Time: 30 min

## Cont. Part Research - Feb 3rd, 2025

I added a few parts to my list.
First up is the motherboard. I will still be reusing the BTT Octopus Pro for the printer, but for the BOM I decided to switch from the SKR mini E3 to a SKR Pico, which is a cheaper option that provides virtually the same functionality.

Since this is a modular industrial 3D printer, I will be having a tool changer with 4 slots. Without the Octopus I have, this would be impossible on normal motherboards. Even using the big motherboard, I would have big problem routing cables for many different toolheads. My best choice is to have a toolhead board that simplifies wiring, and for this I want the BTT EBB 36

I have also decided on the motors: LDO Motors 42STH48-2804AH(S55). These are part of the Super Speedy lineup, and are high temp, high current 1.8 degree motors.

For the motion system I want to use 350mm Mitsumi Linear rails (3 of them) top mounted, and Gate belts

Additions:
- Motherboard on BOM: BTT SKR Pico
- Klipper Host: RPI zero 2 w or a spare SBC I have
- Toolboard: BTT EBB 36
- Carraige CoreXY Motors: LDO 42STH48-2804AH(S55)

Time: 1hr

## Part Research - Feb 2nd, 2025

Today I spent several hours researching parts for my 3D printer that would deliver high performance and fit relatively in budget. I am planning on tearing down a CoreXY printer I already own and redesign from scratch. Some of the parts like the Ender 5 frame can be reused, so the price can be lowered for my prototype. I will still include the total cost with every part I have used, but the price I pay will be lower.

I new right away that the hotend had to have no compromises, so I started looking at hotend similar to the Rapido. I ended up finding the Triangle Labs Rapido ACE, which appears to be the newest and best in the rapido clone lineup. I also considered other hotends like a Bambu Lab or clone. The bambu lab hotends are nice and cheap, but I think they are limited for *super* high speed printing. They are also proprietary. I spent awhile pondering the Phaetus Dragon UHF hotend for awhile, another popular choice. I decided that it was a decent option, but the Rapido hotend had the highest capability. This took most of my research time

For the extruder I am going to go with something I know is stable and strong, the LDO Orbitor 2.0 extruder. This has been running on one of my printer much more reliably than the previous sherpa mini, and I haven't found another extruder that balances price and extrusion force and weight so well.

I also briefly considered Smart Orbiter 3.0 all in one due to the lower price, but this didn't have a super good hotend.

For controlling I know I need something cheap that can support klipper and has TMC drivers. The community disposition seemed to be towards the BigTreeTech E3 v3, so I threw it in without much consideration. The BOM will include this, but in reality I will be reusing a BTT Octopus Pro motherboard from the old printer build, it is super nice and I don't want it to go to waste

I want to use some quality stepper motors, so I will use LDO motors for the carraige, and some cheap motors for the Z- axis

Summary:
- Hotend: Triangle Labs Rapido ACE
- Extruder: LDO Orbiter 2.0 with 36mm pancake motor
- Motherboard: BTT SKR mini E3 (my build will use BTT Octopus Pro)
- 2 Nema 17 motors from LDO 42STH48-something
- 2 nema 17 Ender 3 z-axis motors

Time: 4 hrs

## Concept - Feb 1st, 2025
The basic concept is this: A desktop machine with plug and play heads and beds. Chain these together and add robot carriages in between and you got yourself an awesome factory that can fit in a bench. This is an opensource project. The cost of the _entire system_ will likely be several thousand dollars, with the main machine limited to $300 budget. I aim to lower the cost of a complete industrial system as much as possible.

The head and bed have 2 communication lanes and 2 high power lanes. It is assumed that CAN bus and or USB 3 are used for high reliability.

Time: 30 min
