# Marlin Ender 5 Pro Config

This repository contains a configuration to build Marlin for the Ender 5 Pro with BLTouch for auto bed leveling for the V422 board without the bltouch adapter board.

To build run `./build.sh` and copy the generated bin file to your SD card. 
To flash to your Ender 5 pro just insert the SD card and turn on the Ender 5.

The Configuration in this repository already contains the enablement of the BLTouch. The Config was generated using: 

``` 
git clone git@github.com:MarlinFirmware/Configurations.git
git checkout release-2.0.9.3
```

The contents of [fixes.patch](fixes.patch) were then applied.
