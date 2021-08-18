# 1810-CNC-Addons
How to guide and parts for improving the small CNC milling machines at Fellesverkstedet

### Hoe to make jobs

 - V-Carve pro works well. Make sure you use GRBL post processor when exporting.
 - Bark Beetle also works well. Files with auto setting fr the 1810 machines here: 
 - You can use almost any CAM software that can output plain g-code, like Fusion360 etc. Easel by Shapeoko is an online user friendly simple alternative.

### How to control

 - Universal g-code sender works well: https://winder.github.io/ugs_website/
 - Alternatively you can use any g-coder sender for GRBL
 
### How to fixture material

 - Double sided tape works well

### Tips n tricks

 - The machines are very precise, but very weak. For precision results you almost always need a fishing removing the last 0.05-0.1mm
 - Skim cuts can also work well somtimes (running the samme job  again)


### Axes

 - Absolute max X travel is 172mm - Useful work area with 6mm safety  at start and is **160mm**
 - Absolute max Y travel is 91mm - Useful work area with 5.5mm safety is **80mm**
 - Absolute max Z travel is 43mm - Useful work area with collet nut on is about 36mm. Max thickness of material to cut through *(Bit needs to clear the stock)* is **about 15mm**.
 
### Spindle

 - Max spindle speed seems to be 9200RPM
 - Spindle speed is not linear, so a g-code with for instance a 5000RPM instruction will get a higher RPM than specified.
 - Spindle speed 9000RPM is recommended for convenience and max productivity.
 - Use of a tachometer app or a real tachometer is recommended for lower RPM needs.
 
 
 ### To do
 
  - Make more robust mount for Z homing switch *(can easily move upwards now and not trigger or give inconsistent triggering, screw triggering X limit switch can also shift)*
  - Add e-stop button
  - Finish enclosure, add handle and hinge
  - Tidy up wiring, shorten limit switch cable lengths
  - Improve springloaded preload on acme thread nuts
  - Adjust X and Y axes to be square
  - Adjust Z axis angle to be 90 deg to XY plane
  - Add dust collection solution?
  
  
### Handy GRBL links

 - https://github.com/gnea/grbl/wiki
 - https://linuxcnc.org/docs/2.6/html/gcode/gcode.html
 - https://wiki.shapeoko.com/index.php/G-Code
 - https://wiki.shapeoko.com/index.php/G-Code#Using_the_Work_Coordinate_Systems