# DIY_ESP32_Marauder
# The PCB for an easy DIY version of the ESP32_Marauder project.




# Requirements:

1.- "TFT LCD 2.8" 240x320 SPI ILI9341" (with a SDCard reader) like the one on this site

https://www.aliexpress.us/item/3256805747165796.html choose the board with ILI9341 driver.

2.- ESP32 DevKitC This a 38-Pin board with the chip ESP32-WROOM-32D or the ESP32-WROOM-32U these have the same footprint. 
See here:

https://www.aliexpress.us/item/3256805973309169.html

3.- Iron, solder, headers,etc.

4.- The PCB for the DIY_ESP31_Marauder. Go to the release section of this page and download the ZIP file. Then, upload it your PCB production site of preference.(For example, https://jlcpcb.com/  JLCPCB is cheap) 

# The ESP32 flashing process:

To start, download all the Marauder files needed from the official site (here):

https://github.com/justcallmekoko/ESP32Marauder/wiki/update-firmware

From this site, download the following 4 files for the ESP32 Marauder_v4:

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

(https://github.com/justcallmekoko/ESP32Marauder/wiki/update-firmware) For archival purposes, ease of use as addtional option, a copy of the ESP32_Marauder files version 0.13.6 are inside the BINS folder of this repo. 

Load the bootloader at 0x1000
Load the partitions at 0x8000
Load the Boot app at 0xE000
load the firmware at 0x10000  (_old_hardware.bin)

4.- Finally, when all files are uploaded, click the "program" button.

5.- Solder/Plug your "TFT_LCD 2.8" 240x320 SPI ILI9341" and ESP32-DevKitC to the DIY_Marauder PCB. (Solder/plug the TFT_LCD to the front of the PCB and the ESP32_DevKitC to the back of the PCB. Guide yourself by the ground pins)

6.- Reset yout board, ESP_maruder should boot and show the logo. The DIY_ESP32_Marauder is ready to roll.

Just in case: If the TFT display is not responsive or a bit out of calibration. Then, once again repeat the flashing process this time using the official firmware for the "Marauder_v6" (_new_hardware.bin/_v6.bin).

