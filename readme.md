# EMGauntlet

Based on project at https://hackaday.io/project/8823-super-simple-muscle-emg-sensor/details

Muscles create many action potentials during a movement, like moving your arm or closing your hands. This creates a measurable signal, which shows an increase in signal due to different fingers moving. (Hackaday)

This project extends the Hackaday project to wirelessly communicate the EMG signals to another device.

Why did I make this? Because it's cool. Also, current medical EMG procedures are more invasive and they hurt so this is a better (albeit less precise) alternative. 

### BOM

|Ref                   |Qnty|Value                      |Cmp name                   |Footprint                                                     |Description                                                                                                           |Vendor |Link                                                                                                                                                |
|----------------------|----|---------------------------|---------------------------|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|-------|----------------------------------------------------------------------------------------------------------------------------------------------------|
|C1                    |1   |47uF                       |C                          |Capacitor_SMD:C_0805_2012Metric                               |Unpolarized capacitor                                                                                                 |Digikey|https://www.digikey.com/en/products/detail/samsung-electro-mechanics/CL21A476MQYNNNG/3894447                                                        |
|C2, C3, C4, C5, C6, C7|3   |10uF                       |C                          |Capacitor_SMD:C_0805_2012Metric                               |Unpolarized capacitor                                                                                                 |Digikey|https://www.digikey.com/en/products/detail/taiyo-yuden/LMK212BJ106KG-T/930652                                                                       |
|C8, C9                |2   |1uF                        |C                          |Capacitor_SMD:C_0805_2012Metric                               |Unpolarized capacitor                                                                                                 |Digikey|https://www.digikey.com/en/products/detail/samsung-electro-mechanics/CL21B105KBFNNNE/3886687                                                        |
|D1                    |1   |D                          |D                          |Diode_SMD:D_0805_2012Metric                                   |Diode                                                                                                                 |Digikey|https://www.digikey.com/en/products/detail/kyocera-avx/SD0805S020S0R5/3749524                                                                       |
|D2                    |1   |LED                        |LED                        |LED_SMD:LED_0805_2012Metric                                   |Light emitting diode                                                                                                  |Digikey|https://www.digikey.com/en/products/detail/ams-osram-usa-inc/LG-R971-KN-1-0-20-R18/1227925                                                          |
|D3                    |1   |D_Schottky                 |D_Schottky                 |Diode_SMD:D_SMA                                               |Schottky diode                                                                                                        |Digikey|https://www.digikey.com/en/products/detail/mcc-micro-commercial-components/SK54A-LTP/5114132?s=N4IgTCBcDaIMoGkCsAWAggWgDIBUAKIAugL5A                |
|J1                    |1   |Conn_01x02_Pin             |Conn_01x02_Pin             |Connector_JST:JST_PH_S2B-PH-SM4-TB_1x02-1MP_P2.00mm_Horizontal|Generic connector, single row, 01x02, script generated                                                                |Digikey|https://www.digikey.com/en/products/detail/jst-sales-america-inc/S2B-PH-SM4-TB/926655?s=N4IgTCBcDaIMpgEIFoAKAJZcCyAWZAKogBQAyAYgJTFwBylIAugL5A      |
|J3                    |1   |USB_C_Receptacle_USB2.0_16P|USB_C_Receptacle_USB2.0_16P|Connector_USB:AMPHENOL_12402012E212A                          |USB 2.0-only 16P Type-C Receptacle connector                                                                          |Digikey|https://www.digikey.com/en/products/detail/amphenol-cs-commercial-products/12402012E212A/13683192                                                   |
|R1                    |1   |5.7k                       |R                          |Resistor_SMD:R_0805_2012Metric                                |Resistor                                                                                                              |Amazon |https://www.amazon.com/Yobett-ohm-8850pcs-Resistor-Sample/dp/B013B55KQE?source=ps-sl-shoppingads-lpcontext&ref_=fplfs&smid=A3SC7BPT5ZUZY6&gQT=1&th=1|
|R2                    |1   |1k                         |R                          |Resistor_SMD:R_0805_2012Metric                                |Resistor                                                                                                              |Amazon |https://www.amazon.com/Yobett-ohm-8850pcs-Resistor-Sample/dp/B013B55KQE?source=ps-sl-shoppingads-lpcontext&ref_=fplfs&smid=A3SC7BPT5ZUZY6&gQT=1&th=1|
|R3, R4                |2   |100k                       |R                          |Resistor_SMD:R_0805_2012Metric                                |Resistor                                                                                                              |Amazon |https://www.amazon.com/Yobett-ohm-8850pcs-Resistor-Sample/dp/B013B55KQE?source=ps-sl-shoppingads-lpcontext&ref_=fplfs&smid=A3SC7BPT5ZUZY6&gQT=1&th=1|
|R6, R7, R8            |3   |5.1k                       |R                          |Resistor_SMD:R_0805_2012Metric                                |Resistor                                                                                                              |Amazon |https://www.amazon.com/Yobett-ohm-8850pcs-Resistor-Sample/dp/B013B55KQE?source=ps-sl-shoppingads-lpcontext&ref_=fplfs&smid=A3SC7BPT5ZUZY6&gQT=1&th=1|
|SW1                   |1   |SW_SPST                    |SW_SPST                    |Button_Switch_SMD:SW_DPDT_CK_JS202011JCQN                     |Single Pole Single Throw (SPST) switch                                                                                |Digikey|https://www.digikey.com/en/products/detail/c-k/JS202011JCQN/6137630?s=N4IgTCBcDaIFIGUwAYUEY1wMIEUByIAugL5A                                          |
|SW3, SW4              |2   |SW_Push                    |SW_Push                    |Button_Switch_SMD:SW_TS04-66-50-BK-160-SMT                    |Push button switch, generic, two pins                                                                                 |Digikey|https://www.digikey.com/en/products/detail/cts-electrocomponents/222AMVBAR/5227982                                                                  |
|U1                    |1   |INA128                     |INA128UA                   |Package_SO:SOIC-8-1EP_3.9x4.9mm_P1.27mm_EP2.29x3mm            |Precision, Low Power Instrumentation Amplifier G = 1 + 50kOhm/Rg, DIP-8/SOIC-8                                        |Digikey|https://www.digikey.com/en/products/detail/texas-instruments/INA128UA/300997                                                                        |
|U3                    |1   |MCP73831T-2ACI_OT          |MCP73831T-2ACI_OT          |open-Smartwatch:SOT-23-5                                      |IC CONTROLLR LI-ION 4.2V SOT23-5                                                                                      |Digikey|https://www.digikey.com/en/products/detail/microchip-technology/MCP73831T-2ACI-OT/964301                                                            |
|U4                    |1   |DMG3415U-7                 |DMG3415U-7                 |Package_TO_SOT_SMD:SOT95P240X105-3N                           |                                                                                                                      |Digikey|https://www.digikey.com/en/products/detail/diodes-incorporated/dmg3415u-7/2052768                                                                   |
|U5                    |1   |AP2112K-3.3                |AP2112K-3.3                |Package_TO_SOT_SMD:SOT-23-5                                   |600mA low dropout linear regulator, with enable pin, 3.8V-6V input voltage range, 3.3V fixed positive output, SOT-23-5|Digikey|https://www.digikey.com/en/products/detail/diodes-incorporated/AP2112K-3-3TRG1/4470746?s=N4IgTCBcDaIIIAUwEZlgNIFoDMA6bIAugL5A                       |
|U6                    |1   |ESP32-S3-WROOM-1-N16R2     |ESP32-S3-WROOM-1-N16R2     |RF_Module:ESP32-S3-WROOM-1                                    |                                                                                                                      |Digikey|https://www.digikey.com/en/products/detail/espressif-systems/esp32-s3-wroom-1-n16r8/16162642                                                        |


# Schematic and PCB

Use example circuits. Otherwise you might end up learning too much electrical engineering and that's not good! 
Hardest part was figuring out the footprints because most of the components I used were not in Kicad and its just annoying
PCB was wired up using FreeRouting

# Firmware

Just used the analog read program built into Arduino IDE to collect data

# CAD

This depends HEAVILY on the person and its strongly recommended to use photogrammetry to figure it out properly. Also the electrode placement will vary from person to person. 

![Schematic](https://github.com/Omegon0/emg/blob/main/schematic.jpg?raw=true)
![PCB](https://github.com/Omegon0/emg/blob/main/pcb.jpg?raw=true)
![render1](https://github.com/Omegon0/emg/blob/main/render1.jpg?raw=true)
![render2](https://github.com/Omegon0/emg/blob/main/render2.jpg?raw=true)
