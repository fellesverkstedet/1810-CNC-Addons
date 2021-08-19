# 1810 CNC's

*Guide to the small CNC milling machines at Fellesverkstedet + parts we designed to improve the machines*

![](/Images/1810-at-its-limits-engraving-silver.JPG)


 - Tiny precise milling machines with a 160mm x 80mm x 15mm work area. Slow and weak, but nice for PCB milling, engraving and 3D milling small projects.
 - Commonly called 1810 CNC. Many different variations are sold. We bought ours as kits on [Aliexpress](https://www.aliexpress.com/item/32881076895.html?spm=a2g0s.9042311.0.0.362a4c4dJqbJiP)
 
### How to make jobs

 - V-Carve pro works well. Make sure you use the GRBL post processor when exporting.
 - Bark Beetle also works well. Files with auto setting for the 1810 machines [here](https://github.com/fellesverkstedet/1810-CNC-Addons/tree/master/Maintenance).
 - You can use almost any CAM software that can output plain g-code, like Fusion360 etc. Easel by Shapeoko is an online user friendly simple alternative.

### How to control and send jobs

 - Universal g-code sender works well: https://winder.github.io/ugs_website/
 - Alternatively you can use any g-coder sender for GRBL
 - We like to set up a macro button that homes the machine and sets the correct offsets after homing. Example in the repo [here](https://github.com/fellesverkstedet/1810-CNC-Addons/tree/master/Macros)
 
### How to fixture material

 - Double sided tape works well. We like the tape dispenser type from 3M that can be bought at Jernia
 
 ![](/Images/doublesided-tape-from-jernia.jpg)

### Tips

 - Max spindle RPM is 9200. Feedrates should be half of what you use with the same bit on a ShopBot *(max 18000RPM)*, and pass depths should be lots shallower.
 - The machines are very precise, but very weak. For precision results you almost always need to set up a finishing pass removing the last 0.05-0.1mm.
 - Skim cuts can also work sometimes *(running the same job  again)*


### Axes

 - Absolute max X travel is 172mm - Useful work area with 6mm safety  at start and is **160mm**
 - Absolute max Y travel is 91mm - Useful work area with 5.5mm safety is **80mm**
 - Absolute max Z travel is 43mm - Useful work area with collet nut on is about 36mm. Max thickness of material to cut through *(Bit needs to clear the stock)* is **about 15mm**.
 
### Spindle

 - Max spindle speed seems to be 9200RPM
 - Spindle speed is not linear, so a g-code with for instance a 5000RPM instruction will get a higher RPM than specified.
 - Spindle speed 9000RPM is recommended for convenience and max productivity.
 - Use of a tachometer app or a real tachometer is recommended for lower RPM needs.
 
 
### The add-ons

 - We have developed 3D printed parts for adding homing sensors to the X,Y and Z axis. Files are in this repo [here](https://github.com/fellesverkstedet/1810-CNC-Addons/tree/master/HomingExtensions). We bought [these](https://www.aliexpress.com/item/32842303693.html?spm=a2g0s.9042311.0.0.362a4c4dJqbJiP) homing sensors at Aliexpress.
 - We have developed a 3D printable controller case with a transparent acrylic lid. Files in the repo [here](https://github.com/fellesverkstedet/1810-CNC-Addons/tree/master/ControllerCase)
 - An enclosure is also under development. Files [here](https://github.com/fellesverkstedet/1810-CNC-Addons/tree/master/Enclosure)
 
 ### To do
 
  - Make more robust mount for Z homing switch *(can easily move upwards now and not trigger or give inconsistent triggering, screw triggering X limit switch can also shift)*
  - Add e-stop button
  - Add on/off switch
  - Add safety warning graphics and simple instructions on the machine
  - Finish enclosure, add handle and hinge
  - Tidy up wiring, shorten limit switch cable lengths
  - Add probing plate and wiring for bit length probing *(ala our shopbot setup)*
  - Grease leadscrews?
  - Improve springloaded preload on acme thread nuts *(for increased stiffness)*
  - Adjust X and Y axes to be square
  - Adjust Z axis angle to be 90 deg to XY plane
  - Add dust collection solution?


### PCB milling links

 - https://wiki.bitraf.no/wiki/CNC3-3018Pro  
  
### Handy GRBL links

 - https://github.com/gnea/grbl/wiki
 - https://linuxcnc.org/docs/2.6/html/gcode/gcode.html
 - https://wiki.shapeoko.com/index.php/G-Code
 - https://wiki.shapeoko.com/index.php/G-Code#Using_the_Work_Coordinate_Systems
 
### Gallery

![](/Images/test-engraving-in-pmma.JPG)
*A 32mm x 40mm graphic engraved with a 1mm ball nose and a 60 degree v-bit*


![](/Images/test-in-silver.JPG)
*The same motive in sterling silver, cutouts at 0.1mm pass depth*