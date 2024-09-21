# DIY ESP32 Marauder - Cheapskate version.
![esp32marauder](https://github.com/user-attachments/assets/d4440bb6-f60a-4d18-8730-c3fe9fefdc23)



# This project provides a PCB for an "easy DIY version" of the ESP32_Marauder device.



![Marauder_CheapSkate](https://github.com/user-attachments/assets/e738019d-53d2-460f-a710-94280bb0435b)

# Requirements:

1.- "TFT LCD 2.8" 240x320 SPI ILI9341" (with a SDCard reader) like the one on this site

https://www.aliexpress.us/item/3256805747165796.html choose the board with ILI9341 driver.

2.- ESP32 DevKitC This a 38-Pin board with the chip ESP32-WROOM-32D or the ESP32-WROOM-32U these have the same footprint. 
See here:

https://www.aliexpress.us/item/3256805973309169.html

3.- Iron, solder, headers,etc.

4.- The PCB for the DIY_ESP32_Marauder-Cheapskate version.

Go to the release section of this page and download the ZIP file. Then, upload the zip file to your PCB production site of preference for ordering. 

For example, https://jlcpcb.com/  (JLCPCB is cheap)

Note: While ordering the PCB, I would suggest to choose RED as the PCB color, it would look like as a 'One whole assembly' together with the TFT display (which most times is also RED).


# The ESP32 flashing process:

To start, download all the Marauder files needed from the official site (here):


https://github.com/justcallmekoko/ESP32Marauder/wiki/update-firmware

# Important: 
# It has to be the version v4

From this site, download the following 4 files, for the version "ESP32 Marauder_v4":

1-Bootloader

2-Partitions

3-Boot App

4-Firmware 


Using Google Chrome, we'll flash the ESP32_DevKitC  board with the ESPWebTool from spacehuhn at this site:

https://esp.huhn.me/ 


Then follow these steps carefully:

1.- Plug your ESP32 to your computer and connect.

2.- Select the PORT where your ESP board is connected (serial connection).

3.- Select the corresponding files you downloaded from the official site.

(https://github.com/justcallmekoko/ESP32Marauder/wiki/update-firmware) 

For archival purposes (additional option), a copy of the ESP32_Marauder required files (version 0.13.6) are located in the BINS folder of this repo. 

- Load the bootloader at 0x1000

- Load the partitions at 0x8000

- Load the Boot app at 0xE000

- Load the firmware at 0x10000  (_old_hardware.bin)


4.- Finally, when all files are uploaded, click the "program" button.

5.- Solder/Plug your "TFT_LCD 2.8" 240x320 SPI ILI9341" and ESP32-DevKitC to the front side of the DIY_ESP32Marauder-CheapSkate version PCB. 

 Solder the GPS module to the back side of the PCB. Guide yourself by the ground pins.

6.- Reset your board, the ESP32_Marauder should boot and show the logo. The DIY_ESP32_Marauder is ready to rock and roll.

# PBC Front side of the Cheapskate version- 
Here you will place both the ESP32 and the display

![Marauder_CheapSkate-front](https://github.com/user-attachments/assets/9d4b534e-dc86-4a07-98d0-d08ce4fdfacd)

# PCB back side of the Cheapskate version - 
Here you will solder only the GPS module and a battery (optional).

![Marauder_CheapSkate-back](https://github.com/user-attachments/assets/b607921a-b709-49c0-819a-644fd463900a)



Notes: 
- The back side of the PCB has the silkscreen written ESP32-DevkitC. However, the ESP32-DevKitC goes on the front side.
- Battery (5V) and power switch are optional.
  The Cheapskate version can be powered through the ESP32's USB port or adding a dedicated battery providing 5 volts.
- If the TFT display is not responsive or a bit out of calibration. Then, once again repeat the flashing process this time using the official firmware for the "Marauder_v6" (_new_hardware.bin/_v6.bin).
- If possible support the creator of ESP32_Marauder (justcallmekoko) for his awesome project.
  https://github.com/justcallmekoko/ESP32Marauder




# LICENSE


Distributed under the GNU General Public License v3.0. See LICENSE.txt for more information. 

The tool/device is for educational purpose only and the author does not condone any illegal use. 

Use as your own risk.




  



