# Haori36

![](haori36-keyboard.jpg)

Low-pro 36-key hot-swappable monoblock split ortho keyboard with optional Pimoroni trackball support. 

## Production Files

To manufacture the Haori36 PCB: 

- Use the gerber files in the [production/ folder](production/). Opt for `1.6mm` PCB thickness. 
- The [BOM](production/BOM.csv) and [CPL](production/CPL.csv) files facilitate PCBA services for hassle-free diode soldering. 

The complete PCB project  is in the [kicad/](kicad/) folder. 

## Bill of Materials (BOM)

Quantity | Item 
--- | --- 
1 | RP2040-Zero
1 | Pin headers  
1 | Haori36 PCB 
1 | Haori36 plate 
36 | Kailh Choc V1 switches  
36 | Kailh Choc V1 Hot-swap sockets 
36 | 1N4148 diodes (surface mount, `SOD123`)
1 | Pimoroni Trackball Breakout (optional)

## Case and Plate 

3D print the case with the [STL file](case/haori36-case.stl). The folder also contains an editable [STEP file](case/Haori36-case.step) for customization. 

The plate offers multiple options:

- 3D print using the [STL file](plate/haori36-plate.stl) (or the [no-trackball](plate/haori36-plate-notrakball.stl) version)
- Use PCB material with [gerber files](production/haori36-plate-gerbers.zip) 
- Laser cut with the [DXF file](plate/haori36-plate.dxf)

## Firmware 

The Haori36 comes with precompiled VIA-enabled firmware: 

- Use [penk_haori36_via.uf2](firmware/penk_haori36_via.uf2) for flashing the RP2040-Zero 
- Load the [via.json](firmware/QMK/via.json) file in `Design` tab for [VIA](https://usevia.app) configuration 

The firmware source is located under [firmware/QMK/](firmware/QMK/). The trackball support is enabled by default, and its settings can be adjusted in `keymaps/via/rules.mk` and `keymaps/via/config.h`. 

## Copyright and License
Copyright (c) 2024 Penk Chen. All rights reserved.

All files are licensed under MIT license, see the [LICENSE](LICENSE) for more information.