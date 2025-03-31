- Add a vslot extrusion and wheels for switching off beds. Line up the rails and roll a new bed on
- Hotswap toolheads aren't supported in klipper, so either add this feature or create a macro that modifies the config and reboots klipper each toolrow swap.
- Pogo pins for USB and CAN bus between toolhead an motion carrage
- Use only USB 2.0 to communicate between MCUs because its faster than CAN bus and can support more than klipper data (like hubs and cameras). It also is easier to connect and hotswap, there aren't any resistor configuration requirements. I can use USB 3.0 for static hubs that don't change
- Design a simple converter PCB from XT60 connector and USB C, to the molex special connector
- Design hotswap pcb connectors
- Use JLCMC for all my fasteners, and mcmaster carr for other things


# Tools
dremel
spindle + drill
spindle + milling flute/ball nose mill
router bit
mini sawblade
spindle with grinding wheel / cup
tapmatic-style tap holder
shaper cutter
microscope camera
inkjet cartridge
waterjet cutter
plasma cutter
pencil
exacto holder
glass cutter
sharpie
vibropeen
lasercutter
syringe dispenser
brush + paint pots
hand file
fiber laser holder
mirror X/Y stage
plate-in-place electrode
CMM stylus probe holder
hotwire foam cutter holder
pick-and-place suction tool
soldering iron (w\ solder dispenser ?)
EDM electrode holder