---
title: Flashing Firmware
description: 
published: true
date: 2020-04-11T04:43:36.907Z
tags: 
---

# Flashing Using a Raspberry Pi or Pc running Debian(Without Removing the base)

>Note I have not been successful flashing Earls firmware using this method
{.is-warning}

Tools

An internet connectionRaspberry Pi running some debian/ubuntu flavor (eg octopi or raspbian) Pc with some form of SSH [Like Putty](https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html)

SSH into the pi by typing the ip address into the host name of putty for me its 192.168.1.120.

![pasted_image_0.png](/flashing-assets/pasted_image_0.png)

Enter the username and password the default for raspbian(not your octopi username) is

Username: pi

Password: raspberry

Run the command `sudo apt-get update && sudo apt-get install avrdude` type y when prompted.

![pasted_image_0_(1).png](/flashing-assets/pasted_image_0_(1).png)

Now download the firmware I'm going to download Pinguinpfleger Marlin Firmware using the command `wget https://github.com/pinguinpfleger/ASWX1-FW-MOD/releases/download/ASWX1-FW-MOD-v1.2/ASWX1-FW-MOD-v1.2.zip`

![pasted_image_0_(2).png](/flashing-assets/pasted_image_0_(2).png)

Unzip it with unzip filename you can use the ls command to see a list of files for me it’s ASWX1-FW-MOD-v1.1.zip.
Start the flash with after you replace Name.hex with your hex file name and directory.

`while true; do sudo /usr/bin/avrdude -v -p atmega2560 -c wiring -P $(ls /dev/ttyUSB*) -b 115200 -D -U flash:w:Name.hex:i; if [ "$?" -eq "0" ]; then break; fi; done;`

While the script is running press the reset button next to the tft screen repeatedly until you see AVR Device initialized in the terminal it will then start the flash.
Now run the gcode M502 to reset to firmware defaults then M500 to save.

Flashing the TFT Screen

Download the firmware zip and unzip it
Move the files similar to the ones in the picture to the root of the sdcard. It must be fat32 formatted!!

![pasted_image_0_(3).png](/flashing-assets/pasted_image_0_(3).png)

Plug the SD card into your printer then reboot

# Flashing Using Prusaslicer or Cura