---
id: tpu-settings
title: TPU Settings for 3D printers
---

These settings were tested on Prusa MK4S.
First, loosen the two idler screws approx. 1.5 turns. 
A good method is to loosen the idler screws a little, load the TPU like any other filament, 
and loosen a bit more during the purging phase if the filament is not coming out of the nozzle. 
Don't forget to tighten back up when printing with other filaments.

## Speed for print moves
```
Perimeters: 20
Small perimeters: 20
External perimeters: 20
Infill: 15
Solid infill: 15
Top solid infill: 15
Support material: 15
Gap fill: 15
```

## Speed for non-print moves
`Travel: 150`

## Modifiers
`First Layer Speed: 30`

The Hilbert curve on the bottom might make it easier to pull the print off the plate, 
but is probably not necessary on the top. A textured bed is recommended for easier removal as well. 
