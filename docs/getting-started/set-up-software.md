---
id: set-up-software
title: Set up your software
---

In this chapter, you will learn how to install an [open source slicer](https://slic3r.org/) and set it up. This guide is specific to Glia's equipment, but should be applicable in other situations too.

## Get the software
For this guide, we will use the [Prusa Edition of Slic3r](https://www.prusa3d.com/slic3r-prusa-edition/), though [the regular Slic3r](https://slic3r.org) also works well and should be usable.

Start by downloading the software from the site below:
* [https://github.com/prusa3d/Slic3r/releases](https://github.com/prusa3d/Slic3r/releases)

### GNU/Linux
* Download the AppImage file.
* Make the file executable like so: `chmod +x <filename>.AppImage`
* If you are using Ubuntu, right click on the AppImage file, select properties and enable execution.
* Start the program by double-clicking on it or executing from commandline.

### Mac OSX
* Get the dmg file
* Install the files inside it

### Windows
* Get the win64 zip (unless you know you need win32).
* Launch the executable inside

## Start and configure Slic3rPE
Once the software is installed, go ahead and start up Slic3rPE. In the configuration wizard, pick the profiles for the MK3, the MK2.5, and the SL1. The Glia Project uses Prusa [MK3s](https://www.prusa3d.com/original-prusa-i3-mk3/), an MK2.5, several MK3 clones that we built in-house and a [Wanhao Duplicator 7](http://www.wanhao3dprinter.com/Unboxin/ShowArticle.asp?ArticleID=81) that resembles the SL1.

### Enable background processing
Background processing will make your life easier and allow Slic3r to slice in the background as you make changes, speeding up the final export.

* Go to Configuration -> Preferences
* Select "Background processing"

### Download our Glia-specific profiles - coming soon
This step is not operational yet and is coming soon. For now, simply use the default profiles.

## Ready for takeoff!
You are now ready to find a model and slice your first print!