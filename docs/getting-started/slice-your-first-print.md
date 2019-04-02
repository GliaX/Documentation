---
id: slice-your-first-print
title: Slice your first print
---
## Enter the Glia printer settings
The default settings are good, but don't seem to work very well with the filament and printers that we use. Instead, change the following settings:

### Filament settings - PLA
* First layer temperature: 230
* First layer bed: 70
* Other layers bed: 70

### Filament settings - PETG
* First layer nozzle temperature: 265
* Other layers nozzle temperature: 240
* First layer bed: 90
* Other layers bed: 80

## Import your model
* Click the "Add..." button in the top icon toolbar
* Select your STL model file that you downloaded in the previous step

You should now see your model!

## Scale your model
Sometimes the scale of the model is too small or too big. Go ahead and select the model, then find the "scale" settings on the right hand toolbar. Grow or shrink the number. The axes should be locked so they are all scaled together.

## Orient your model
Sometimes the model is standing when it should be lying flat or vice versa. You can rotate the model as needed on the three axes until it's appropriate. Note that if your mouse touches the white axis lines, you will snap to them. This is almost always the correct way to rotate.

## Does your model need supports?
The printer will deposit melted plastic. This means that it has to be deposited on something. While small gaps can be bridged between two areas, you cannot print into thin air. In those cases, you need to enable supports.

To do this, select "Print Settings", "Support Material", and then check off "Generate support material".

## Preview your work
Once you are happy, take a look at the preview. Make sure there are no sudden layers that appear and are printed in air, and that the print appears correct.

## Set the Glia printer profile
* Enable "Expert mode"
* In "Printer settings", go to "Custom G-Code"
* Replace the contents of "Start G-code" with the following:

```
M80 ; Turn printer power supply on
M83  ; extruder relative mode
M140 S[first_layer_bed_temperature] ; set bed temp
M104 S[first_layer_temperature] ; set extruder temp
M190 S[first_layer_bed_temperature] ; wait for bed temp
M109 S[first_layer_temperature] ; wait for extruder temp
; Retract filament to prevent oozing
G92 E0 ; reset extruder location
G1 F500 E-8 ; retract by -8
G92 E0 ; reset again

G28 ; home all without mesh bed level
G29 ; Auto bed level
;G29 P0; Wipe old mesh
;G29 P1; mesh bed leveling
;G29 P3 T; mesh bed leveling
;G29 F 10.0; Fade height for correction at 10.0mm
;G29 A; Activate Mesh bed leveling

;M421 I0 J0 Q-0.2 ; Correct front left point
;M421 I0 J1 Q-0.2 ; Correct middle left point
;M421 I0 J2 Q-0.2 ; Correct back left point

M421 I2 J0 Q+0.2 ; Correct front right point
M421 I2 J1 Q+0.2 ; Correct back right point
M421 I2 J2 Q+0.2 ; Correct back right point
G1 X0 Y-1 Z0.2 F4000.0 ; go outside print area
G1 X60.0 E9.0  F1000.0 ; intro line
G1 X100.0 E12.5  F1000.0 ; intro line
```

## Export the G Code
First make sure the correct printer has been selected (MK2.5, MK3, or the custom as above). Also select 0.20 for your layer height.

Export the G Code to the SD Card by selecting the "Export G-Code" button. Select the SD card's location to export to.

## Save the project for later
In case you want to come back to this project later, go ahead and save it to your hard drive. Do this with "File" > "Save Project".
