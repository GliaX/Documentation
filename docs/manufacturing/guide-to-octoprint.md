---
id: guide-to-octoprint
title: Guide to Octoprint
---

[Octoprint](https://octoprint.org) is described by its creator as being somewhere between a "baby monitor" and a "remote control" for 3D printers. It allows for monitoring and control of prints remotely.

## Logging in
Go to the URL as provided. You will see a certificate problem. You can go ahead and accept the certificate
![Certificate problem](assets/media/octoprint-01.png)
![Certificate problem](assets/media/octoprint-02.png)
 
You will now see the main status page that shows the current progress, temperature and what file is being printed:
![Octoprint status page](assets/media/octoprint-03.png)

From this page, you can pause the print or cancel it if needed.

## Monitoring
You can select the **Control** tab to get a video of the printer bed, which will look like the image below.
![Octoprint status page](assets/media/octoprint-04.png)

The camera is at an angle that does not permit easy assessment of small blemishes in the print, but it should show any catastrophes that require cancellation.

## Canceling an object
There are two ways to cancel an object. To get a list of objects, click on the hamburger menu on the right and select the **Cancel objects** tab. This is hard for us since we use so many repetitive objects that are named non-intuitively.

More intuitive is the GCode viewer page. Select the **GCode Viewer** tab and allow it to process the gcode. It will present you with orange dots. Note that the orange dots are not exactly over the object they represent, so use your judgment on which object to cancel. Note the red markings on the image for examples.

![Octoprint status page](assets/media/octoprint-05.png)
