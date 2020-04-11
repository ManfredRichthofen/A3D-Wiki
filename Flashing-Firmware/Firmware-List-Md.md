---
title: Firmware List
description: 
published: true
date: 2020-04-11T04:25:47.551Z
tags: 
---

# Sidewinder X1
## Earl Miller SWX1 (Marlin 1.1.9)
- [Earl Millers Paypal *PlaceHolder*](https://www.paypal.me/ancientwolfgr)
- [3D Nexus Website *PlaceHolder*](https://3d-nexus.com/)
- [Firmware Downloads](https://3d-nexus.com/resources/file-archives/download/5-printer-firmware/11-artillery-swx1-marlin-1-1-9-advanced-firmware-and-gui)
{.links-list}

**Features:**

Save to EEPROMEnabled EEPROM to persist settings. Now you can store PIDs and Z offsets to EEPROM.

P.I.D. Auto-tune - Extruder AND Bed In One OperationPID Tuning improves your hotend/bed temperature stability and will positively impact print quality. This command initiates a process of heating and cooling to determine the proper PID values for your hotend. This may take up to 10 minutes. During the tuning process the LED will stay Red. Once the process is finished, the LED will turn Green. Make sure you wait! Your machine specific PID values are now in use. However, if you want to persist your PID settings you must execute “Store to EEPROM”.

Mesh Bed LevelingMesh Bed Leveling (MBL) allows interactively measuring a Z height mesh without a bed probe (like BLTouch or similar). The only tool required is a piece of paper or a feeler gauge. MBL uses the mesh to compensate for variations in height across the bed. You simply begin the probing and hit save at point 9. I will include a tutorial and perhaps a video demonstrating this process.  There are some important notes below in the tutorial section. Make sure you read them.

Linear AdvanceLinear Advance is now activated, but the set the K_Factor to 0, so it is disabled. To enable it using gcode you should first calibrate your specific K factor. You can do this here. Accordingly set the K factor within your slicer or command interface using e.g. M900 K0.2 (as an example)

Preheat Preset for PLA

Its with the PID Auto-tune and MBL section to keep things tidy- it lets you easily preheat to given preset, you can change the temps in the mks_config.txt.

Live Adjust Z / Baby-stepping ZDuring printing the first layer you can still adjust the distance between the nozzle and the print-bed. E.g. if you find your print is not sticking you can carefully step down the nozzle or correct it up again without the need to re-level all four screws at the same time. However, this assumes the bed is in level overall but maybe just a little too low or too high overall. You need to execute Store To EEPROM to persist Z Values. (There is a Save to EEPROM in the interface for this)

## Pinguinpfleger SWX1 (Marlin 2.X.X)
- [Firmware Downloads](https://www.google.com)
- [TFT Firmware Download](https://www.google.com)
{.links-list}

**Features:**

P.I.D. Auto-Tune

PID Tuning improves your hotend/bed temperature stability and will positively impact print quality. This command initiates a process of heating and cooling to determine the proper PID values for your hotend. This may take up to 5 minutes. During the tuning process the LED will stay Red. Once the process is finished, the LED will turn Green. Make sure you wait! Your machine specific PID values are now in use. However, if you want to persist your PID settings you must execute “Store to EEPROM”

Save to EEPROMEnabled EEPROM M500 to persist settings.Now you can store PIDs and Z-Offsets to EEPROM

LINEAR ADVANCE activatedLinear Advance brings you better dimensional precision due to reduced bleeding edges.Higher printing speeds are possible without any loss of print quality - as long as your extruder can handle the needed speed changes.Visible and tangible print quality is increased even at lower printing speeds.No need for high acceleration and jerk values to get sharp edges.Read https://marlinfw.org/docs/features/lin_advance.html for more details and how to calibrate.By default the K_Factor is set to 0, so it is disabled.To enable it using gcode you should first calibrate your specific K factor.You can do this here. Accordingly set the K factor within your slicer using e.g. M900 K0.2

S_CURVE ACCELERATION activatedThis option eliminates vibration during printing by fitting a Bézier curve to move acceleration, producing much smoother direction changes.

ADAPTIVE STEP SMOOTHING activatedAdaptive Step Smoothing increases the resolution of multi-axis moves, particularly at step frequencies below 1kHz (for AVR) or 10kHz (for ARM), where aliasing between axes in multi-axis moves causes audible vibration and surface artifacts. The algorithm adapts to provide the best possible step smoothing at the lowest stepping frequencies.

Live Adjust Z / Baby-stepping Z

During printing the first layer you can still adjust the distance between the nozzle and the print-bed. E.g. if you find your print is not sticking you can carefully step down the nozzle or correct it up again without the need to re-level all four screws at the same time. However, this assumes the bed is in level overall but maybe just a little too low or too high overall. You need to execute Store To EEPROM to persist Z Values.

## Waggster Mod BLTouch Artillery SWX1 (Marlin 1.19)

- [Firmware Downloads](https://pretendprusa.co.uk/index.php?action=downloads;cat=5)
- [Bltouch Mount](https://www.thingiverse.com/thing:3716043)
{.links-list}

**Features:**

P.I.D. Auto-Tune

PID Tuning improves your hotend/bed temperature stability and will positively impact print quality. This command initiates a process of heating and cooling to determine the proper PID values for your hotend. This may take up to 5 minutes. During the tuning process the LED will stay Red. Once the process is finished, the LED will turn Green. Make sure you wait! Your machine specific PID values are now in use. However, if you want to persist your PID settings you must execute “Store to EEPROM”

Bl-Touch an auto leveling sensor for 3D Printers that can precisely measure the tilt of Bed surface. It works with most kinds of bed materials, such as glass, wood, and metals.


# Genius
## Earl Miller Genius (Marlin 1.1.9)
- [Earl Millers Paypal *PlaceHolder*](https://www.paypal.me/ancientwolfgr)
- [3D Nexus Website *PlaceHolder*](https://3d-nexus.com/)
- [Firmware Downloads](https://3d-nexus.com/resources/file-archives/download/5-printer-firmware/12-artillery-genius-marlin-1-1-9-advanced-firmware-and-gui)
{.links-list}

**Features:**

Save to EEPROMEnabled EEPROM to persist settings. Now you can store PIDs and Z offsets to EEPROM.

P.I.D. Auto-tune - Extruder AND Bed In One OperationPID Tuning improves your hotend/bed temperature stability and will positively impact print quality. This command initiates a process of heating and cooling to determine the proper PID values for your hotend. This may take up to 10 minutes. During the tuning process the LED will stay Red. Once the process is finished, the LED will turn Green. Make sure you wait! Your machine specific PID values are now in use. However, if you want to persist your PID settings you must execute “Store to EEPROM”.

Mesh Bed LevelingMesh Bed Leveling (MBL) allows interactively measuring a Z height mesh without a bed probe (like BLTouch or similar). The only tool required is a piece of paper or a feeler gauge. MBL uses the mesh to compensate for variations in height across the bed. You simply begin the probing and hit save at point 9. I will include a tutorial and perhaps a video demonstrating this process.  There are some important notes below in the tutorial section. Make sure you read them.

Linear AdvanceLinear Advance is now activated, but the set the K_Factor to 0, so it is disabled. To enable it using gcode you should first calibrate your specific K factor. You can do this here. Accordingly set the K factor within your slicer or command interface using e.g. M900 K0.2 (as an example)

Preheat Preset for PLA

Its with the PID Auto-tune and MBL section to keep things tidy- it lets you easily preheat to given preset, you can change the temps in the mks_config.txt.

Live Adjust Z / Baby-stepping ZDuring printing the first layer you can still adjust the distance between the nozzle and the print-bed. E.g. if you find your print is not sticking you can carefully step down the nozzle or correct it up again without the need to re-level all four screws at the same time. However, this assumes the bed is in level overall but maybe just a little too low or too high overall. You need to execute Store To EEPROM to persist Z Values. (There is a Save to EEPROM in the interface for this)