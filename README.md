# Customized Marlin Firmware for 3DRaion Printer.

<img align="top" width=175 src="buildroot/share/pixmaps/logo/Raion_Logo.png" /> 

Customized firmware version for use with 3D raion Printer and 3D Raion Printer with diamond hotend.

Based on Marlin 3D Printer Firmware, RC07

## Changes from Marlin
- Change firmware version to 2.0.1: Configuration.h and Configuration_adv.h changed version to 010101
- Refactor the LCD Menus to be conformed with the current menus of 3D Raion Printers
- If Mixing extruder is used, we still have the possibility of control each extruder's motor individually 
- LCD encoder rotation invert
- add Version query gcode (M283)

## Recent Changes in Marlin (vs Marlin 1.0.2-1)
- RC7 - 31 Jul 2016
  - Add Print Job Timer and Print Counter (`PRINTCOUNTER`)
  - New `M600` Filament Change (`FILAMENT_CHANGE_FEATURE`)
  - New `G12` Nozzle Clean (`NOZZLE_CLEAN_FEATURE`)
  - New `G27` Nozzle Park (`NOZZLE_PARK_FEATURE`)
  - Add support for `COREYZ`
  - Add a new Advance Extrusion algorithm (`LIN_ADVANCE`)
  - Add support for inches, Fahrenheit, Kelvin units (`INCH_MODE_SUPPORT`, `TEMPERATURE_UNITS_SUPPORT`)
  - Better handling of `G92` shifting of the coordinate space
  - Add Greek and Croatian languages
  - Improve the Manual (Mesh) Bed Leveling user interface
  - Add support for more boards, controllers, and probes:
    - Vellemann K8400 (`BOARD_K8400`)
    - RigidBot V2 (`BOARD_RIGIDBOARD_V2`)
    - Cartesio UI (`BOARD_CNCONTROLS_12`)
    - BLTouch probe sensor (`BLTOUCH`)
    - Viki 2 with RAMPS and MKS boards
  - Improve support for `DELTA` and other kinematics
  - Improve thermal management, add `WATCH_BED_TEMP_PERIOD`
  - Better handling of toolchange, multiple tools
  - Add support for two X steppers `X_DUAL_STEPPER_DRIVERS`
  - Add support for `SINGLENOZZLE`, `MIXING_EXTRUDER`, and `SWITCHING_EXTRUDER`
  - Simplified probe configuration, allow usage without bed leveling
  - And much more… See the [1.1.0-RC7 Change Log](https://github.com/MarlinFirmware/Marlin/releases/tag/1.1.0-RC7) for the complete list of changes.

- RC6 - 24 Apr 2016
  - Marlin now requires Arduino version 1.6.0 or later
  - Completed support for CoreXY / CoreXZ
  - See the [1.1.0-RC6 Change Log](https://github.com/MarlinFirmware/Marlin/releases/tag/1.1.0-RC6) for all the changes.

- RC5 - 01 Apr 2016
  - Warn if compiling with older versions (<1.50) of Arduino
  - Fix various LCD menu issues
  - Add formal support for MKSv1.3 and Sainsmart (RAMPS variants)
  - Fix bugs in M104, M109, and M190
  - Fix broken M404 command
  - Fix issues with M23 and "Start SD Print"
  - More output for M111
  - Rename FILAMENT_SENSOR to FILAMENT_WIDTH_SENSOR
  - Fix SD card bugs
  - and a lot more
  - See the [1.1.0-RC5 Change Log](https://github.com/MarlinFirmware/Marlin/releases/tag/1.1.0-RC5) for more!

- RC4 - 24 Mar 2016
  - Many lingering bugs and nagging issues addressed
  - Improvements to LCD menus, CoreXY/CoreXZ, Delta, Bed Leveling, and more…

- RC3 - 01 Dec 2015
  - A number of language sensitive strings have been revised
  - Formatting of the LCD display has been improved to handle negative coordinates better
  - Various compiler-related issues have been corrected

- RC2 - 29 Sep 2015
  - File styling reverted
  - LCD update frequency reduced

- RC1 - 19 Sep 2015
  - Published for testing

## Submitting Patches
Proposed patches should be submitted as a Pull Request against the [RCBugFix](https://github.com/BelovedTutu/Marlin-FW-fork/tree/RCBugFix) branch.

- Don't submit new feature proposals. The RCBugFix branch is for fixing bugs in existing features.
- Do submit questions and concerns. The "naive" question is often the one we forget to ask.
- Follow the proper coding style. Pull requests with styling errors will be delayed. See our [Coding Standards](https://github.com/MarlinFirmware/Marlin/wiki/DNE-Coding-Standards) page for more information.

## Current Status: Testing

Please test this firmware and inform us if it misbehaves in any way. Volunteers are standing by!

[![Travis Build Status](https://travis-ci.com/BelovedTutu/Marlin-FW-fork.svg?token=ScTS197SYABVsXxmanxK&branch=DiamondHotend)](https://travis-ci.com/BelovedTutu/Marlin-FW-fork)

##### [RepRap.org Wiki Page](http://reprap.org/wiki/Marlin)

## Credits

The current Marlin dev team consists of:

 - Scott Lahteine [@thinkyhead] - English
 - [@Wurstnase] - Deutsch, English
 - F. Malpartida [@fmalpartida] - English, Spanish
 - Jochen Groppe [@CONSULitAS] - Deutsch, English
 - [@maverikou]
 - Chris Palmer [@nophead]
 - [@paclema]
 - Edward Patel [@epatel] - Swedish, English
 - Erik van der Zalm [@ErikZalm]
 - David Braam [@daid]
 - Bernhard Kubicek [@bkubicek]
 - Roxanne Neufeld [@Roxy-3DPrintBoard] - English

More features have been added by:
  - Alberto Cotronei [@MagoKimbra]
  - Lampmaker,
  - Bradley Feldman,
  - and others...

## License

Marlin is published under the [GPL license](/LICENSE) because we believe in open development. The GPL comes with both rights and obligations. Whether you use Marlin firmware as the driver for your open or closed-source product, you must keep Marlin open, and you must provide your compatible Marlin source code to end users upon request. The most straightforward way to comply with the Marlin license is to make a fork of Marlin on Github, perform your modifications, and direct users to your modified fork.

While we can't prevent the use of this code in products (3D printers, CNC, etc.) that are closed source or crippled by a patent, we would prefer that you choose another firmware or, better yet, make your own.

[![Flattr this git repo](http://api.flattr.com/button/flattr-badge-large.png)](https://flattr.com/submit/auto?user_id=ErikZalm&url=https://github.com/MarlinFirmware/Marlin&title=Marlin&language=&tags=github&category=software)
