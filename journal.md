---
Title: "Muscle EMG sensor"
Author: "Padimo"
Description: "Uses little currents in muscles to detect muscle movement"
Created On: "14/7/2025"
---

# July 12th

Used the Hackaday schematic as a starting point. Also added an ESP32 module and some power management (battery charging and power switching is HARD). Schematic is done, just need to add footprints and then make the PCB.

![Schematic](https://github.com/Omegon0/emg/blob/main/schematic.jpg?raw=true)

Time spent: 4h

# July 13th

Fixed all errors and passed ERC. Also added footprints to all components. 
Threw stuff into PCB, organized everything, and autorouted. Everything fits onto the top layer 65mmx42mm!
It's looking more like a gauntlet sort of than a slim band but that's ok since it's using a lot of larger components. 

![PCB](https://github.com/Omegon0/emg/blob/main/pcb.jpg?raw=true)

Time spent: 5h

# July 14th

Caught a few mistakes here and there, and generated production files. Still need to mess around with JLCPCB assembly and see what can be done there.

Time spent: 2h

# July 15th

Started BOM. For the IC footprints that I used, I don't know the pitch... I'll need to fix everything with the INA128.

Time spent: 3h

![BOM](https://github.com/Omegon0/emg/blob/main/bom.jpg?raw=true)

# July 16th

Done with BOM, fixed everything. But there were some crazy high MOQs so I found ones that didn't have that. 

Some components are to be hand soldered: resistors and the power switch. The "additional BOM" is here:

| Item | Quantity | Price | Link |
| CUS-12TB | 1 | $0.86 | https://www.digikey.com/en/products/detail/nidec-components-corporation/CUS-12TB/1124222 |
| 0805 resistors | 1 | depends but I have them | N/A |
| tactile switches | 2 | again, depends but I have them | https://www.digikey.com/en/products/detail/cts-electrocomponents/222AMVBAR/5227982 | 

i just wanted to make a table they're cool

Also J2 is supposed to be a solderable header so nothing is needed there

Time spent: 3h

**Total time spent: 17h**
