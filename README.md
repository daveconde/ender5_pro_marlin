# Marlin Ender 5 Pro Config

This repository contains a configuration to build Marlin for the Ender 5 Pro with BLTouch for auto bed leveling for the V422 board without the bltouch adapter board.

To build run [./build.sh](build.sh) and copy the generated bin file to your SD card. 
To flash to your Ender 5 pro just insert the SD card and turn on the Ender 5.

The Configuration in this repository already contains the enablement of the BLTouch. The Config was generated using: 

``` 
git clone git@github.com:MarlinFirmware/Configurations.git
git checkout release-2.0.9.3
```

The contents of [fixes.patch](fixes.patch) were then applied.

# Using Cura

I'm using [octoprint](https://octoprint.org/) on a Pi 4. When using with an Ender 5 Pro the USB on the Pi back feeds power to the printer. Using a USB power blocker [adapter](https://www.amazon.co.uk/PortaPow-USB-Power-Blocker-Cased/dp/B094FYL9QT) fixes the back powering.

To use [Cura](https://ultimaker.com/software/ultimaker-cura) I installed [OctoPrint Connection Plugin](https://marketplace.ultimaker.com/app/cura/plugins/fieldofview/OctoPrintPlugin) via the Cura Marketplace. The printer needs to be added as a local Ender 5 and then configured under manage printers -> Connect to OctoPrint.

To enable Auto Bed Leveling in Cura you need to add `G29 ;Leveling` code under `G28 ;Home` in Start G-Code under the machine settings menu.
