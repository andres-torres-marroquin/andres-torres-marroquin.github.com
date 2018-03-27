---
layout: post
title: "Zelda 1 Overworld pixel map"
description: "Zelda 1 Overworld pixel map"
category: personal
tags: [3d-printing,3dprinting]
---
{% include JB/setup %}

Based on the great map modeled by DarkApollo https://www.thingiverse.com/thing:2138498

[![Zelda Overword 3D Printed Pixel Map](https://img.youtube.com/vi/mMalvPH9m8g/0.jpg)](https://www.youtube.com/watch?v=mMalvPH9m8g)

#### STL Files
I fixed a bunch of STL files and uploaded them to Github: https://github.com/andres-torres-marroquin/zelda-overworld-pixel-map

Still Slic3r fails to slice them correctly, I used Slic3r Prusa Edition, it works much better and faster.

#### Filaments Used
It weights roughly 500 grams worth of filament. I printed them on different materials, using the [M600](http://marlinfw.org/docs/gcode/M600.html) color change on gcode, so no painting was required. (I'm too lazy for that lol)
 - Gizmo Dorks Beige 1.75mm PLA
 - Gizmo Dorks Blue 1.75mm PLA
 - Hatchbox Green 1.75mm PLA
 - Hatchbox White 1.75mm PLA
 - Hatchbox Gray 1.75mm PLA
 - Filamentum Extrafill Signal Brown 1.75mm PLA

#### How to M600 Properly (WIP)
Examples to understand this guide, remember that the first layer is commonly 0.2mm:
 - Printing E7 at 0.2mm resolution - 10 layers (0.2mm-2.0mm) are beige, then 2.2mm to end a are green.
 - Printing E7 at 0.15mm resolution - 13 layers (0.2mm-2.0mm) are beige, then 2.2mm to end are green.
 - Printing E7 at 0.1mm resolution - 20 layers (0.2mm-2.0mm) are beige, then 2.2mm to end are green.

##### Beige 0.0mm to 2.0mm - Green 2.0mm to end (26 pieces)
 - E7 E8
 - G7 G8
 - H6 H7 H8
 - I6 I7 I8
 - J5
 - K5
 - L5 L6 L7
 - M4 M5 M6 M7
 - N4 N5 N6 N7
 - O5 O6 O7

##### Blue 0.0mm to 1.0mm - Beige 1.0mm to 2.0mm - Green 2.0mm to end (12 pieces)
 - E6
 - F6 F7 F8
 - G5 G6
 - H5
 - I5
 - J6 J7
 - K6 K7


##### Beige 0.0mm to 2.0mm - Brown 2.0mm to end (25 pieces)
 - A7 A8
 - B6 B7 B8
 - C2 C6 C7 C8
 - D2 D6 D7 D8
 - E2
 - F2
 - G2
 - J3 J8
 - K3 K4 K8
 - L3 L4
 - M3
 - P2

##### Blue 0.0mm to 1.0mm - Beige 1.0mm to 2.0mm - Brown 2.0mm to end (27 pieces)
 - C5
 - D5
 - E4 E5
 - F4 F5
 - G3 G4
 - H2 H3 H4
 - I3 I4
 - J4
 - L8
 - M8
 - N3 N8
 - O2 O3 O4 O8
 - P4 P5 P6 P7 P8

##### Gray 0.0mm to 2.0mm - White 2.0mm to end (1 pieces)
 - A6

##### Gray 0.0mm to 10.0mm - White 10.0mm to end (6 pieces)
 - A3 A4 A5
 - B3 B4 B5

##### Blue 0.0mm to 1.0mm - Gray 1.0mm to 2.0mm - White 2.0mm to end (1 pieces)
 - P3

##### Brown 0.0mm to 9.0mm - Beige 9.0mm to 10.0mm - Brown 10.0mm to end (4 pieces)
 - A2
 - B2
 - E3
 - F4

##### Brown 0.0mm to 17.0mm - Beige 17.0mm to 18.0mm - Brown 18.0mm to end (1 pieces)
 - C3

##### Brown 0.0mm to 19.0mm - Beige 19.0mm to 20.0mm - Brown 20.0mm to end (4 pieces)
 - A1
 - B1
 - C1
 - D1

##### Brown 0.0mm to 22.0mm - Beige 22.0mm to 23.0mm - Brown 23.0mm to end (6 pieces)
 - E1
 - F1
 - G1
 - H1
 - I1
 - J1

##### Brown 0.0mm to 14.0mm - Beige 14.0mm to 15.0mm - Brown 15.0mm to end (1 pieces)
 - L1

##### Brown 0.0mm to 13.0mm - Beige 13.0mm to 14.0mm - Brown 14.0mm to end (2 pieces)
 - M1
 - N1



#### Video
Here is a small video I made about it: https://www.youtube.com/watch?v=mMalvPH9m8g
