# Inkscape Notes
- You can convert paths to filled objects using union and strokes or objects to paths and all sorts of fun combos
- If you go into object properties you can custom name SVG items!
- Use Path Combine or Break Apart tools to give paths a common stroke and color, even if they aren't connected. Boolean ops are for connections

# Process for creating Logo types
1. Create the base color logo. Use offset live path effect with rounded corners and then flatten it to a normal object for the internal light colors. More control than the Path Outset tool. Break it apart and delete the weird extra small shapes. Make sure to name all objects, and have a layer for the printer and layer for the burn
2. Copy and start on two-tone version. Delete the 3rd inset color. Make sure the color pallet only has Primary and Background colors. Change all lines to Primary color, and make sure everything else is a fill color. Re-create the burn internal offset except without internal edges. The burn has to go behind the printer now.
3. Copy and start on black and white version. Only change necessary, which should just be the colors
4. For Mono, take the path difference of the trail and the background so that you have no background fill object. Delete the fill object for the printer. Now it should be transparent and have only one color
5. Finally, to get a logo that can be extruded in 3D, convert all strokes to paths, boolean union on all paths, Get ride of all groups and layers, and save as a DXF R14 file without changing any of the defaults. 
