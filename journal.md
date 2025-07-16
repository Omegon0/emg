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
| JS202011JCQN | 1 | 0.84 | https://www.digikey.com/en/products/detail/c-k/JS202011JCQN/6137630?s=N4IgTCBcDaIFIGUwAYUEY1wMIEUByIAugL5A |
| 0805 resistors | 1 | depends but I have them | N/A |
| tactile switches | 2 | again, depends but I have them | https://www.digikey.com/en/products/detail/cts-electrocomponents/222AMVBAR/5227982 | 
| ESP32 S3 N16 | 1 | 5.92 | https://www.digikey.com/en/products/detail/espressif-systems/ESP32-S3-WROOM-1-N16/16162647 |
| SD0805S020S0R5 | 1 | 0.34 | https://www.digikey.com/en/products/detail/kyocera-avx/SD0805S020S0R5/3749524 | 

Also J2 is supposed to be a solderable header so nothing is needed there

### Problems
I uploaded everything to JLCPCB and it turns out that the ESP can't be mounted with economic assembly so that's another one to add to the list. 
Diode that I used was a BAT54 but the footprint was 0805 and its better to do that on my own so that's added to this extra BOM
Some ICs were rotated -90 degrees so I fixed that in the CLS file

I am now discovering the extended component fee. I'm switching to stencil and doing it myself, and I'll figure it all out tomorrow

Time spent: 6h

# July 17



**Total time spent: 20h**
