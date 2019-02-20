---
id: slice-your-first-print
title: Slice your first print
---
## Enter the Glia printer settings
The default settings are good, but don't seem to work very well with the filament and printers that we use. Instead, change the following settings:

### Filament settings
* First layer temperature: 230
* First layer bed: 70
* Other layers bed: 70

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

## Export the G Code
First make sure the correct printer has been selected (MK2.5 or MK3)

Export the G Code to the SD Card by selecting the "Export G-Code" button. Select the SD card's location to export to.

## Save the project for later
In case you want to come back to this project later, go ahead and save it to your hard drive. Do this with "File" > "Save Project".
