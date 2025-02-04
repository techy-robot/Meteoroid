# Overview
Production-ready 3d printer based on a Ender 5 frame, with multifunction tool changing.

A desktop machine with plug and play heads and beds. Chain these together and add robot carriages in between and you got yourself an awesome modular factory that can fit in a bench. This is an opensource project. The cost of the _entire system_ will likely be several thousand dollars, with the main machine limited to $300 budget. I aim to lower the cost of a complete industrial system as much as possible.

The base machine is a CoreXY printer with a 500+mm/s move speed and 30k+ accel, 4 tool changer slots for Drill bits, Pick-n-place, 3D printer heads, or lasers. The printer is partially enclosed, with several openings for robots to quick swap tools and beds and sometimes even sub-tools (Like a pnp head with different nozzle sizes).

Total Aggrigate Hours Spent: 5.5 hrs
Project Time Span: Feb 1, 2025-

# Log
## Cont. Part Research - Feb 3rd, 2025

I added a few parts to my list.
First up is the motherboard. I will still be reusing the BTT Octopus Pro for the printer, but for the BOM I decided to switch from the SKR mini E3 to a SKR Pico, which is a cheaper option that provides virtually the same functionality.

Since this is a modular industrial 3D printer, I will be having a tool changer with 4 slots. Without the Octopus I have, this would be impossible on normal motherboards. Even using the big motherboard, I would have big problem routing cables for many different toolheads. My best choice is to have a toolhead board that simplifies wiring, and for this I want the BTT EBB 36

I have also decided on the motors: LDO Motors 42STH48-2804AH(S55). These are part of the Super Speedy lineup, and are high temp, high current 1.8 degree motors.

For the motion system I want to use 350mm Mitsumi Linear rails (3 of them) top mounted, and Gate belts

Additions:
- Motherboard on BOM: BTT SKR Pico
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
