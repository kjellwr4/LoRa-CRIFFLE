# LoRa-CRIFFLE
This repository contians instructions, resources, and code for building the LoRa version of the CRIFFLE.
# LoRaWAN Gateway
A LoRaWAN gateway is... A good explanation of the benefits and drawbacks are illustrated in this video...
## Items
* [ESP32 LoRa 1-Channel Gateway](https://www.sparkfun.com/products/14893)
* [Pycom LoRa and Sigfox Antenna Kit- 915Mhz](https://www.sparkfun.com/products/14676)
* Micro-USB Cable and Wall Wart
## Resources
* [Sparkfun Tutorial](https://learn.sparkfun.com/tutorials/esp32-lora-1-ch-gateway-lorawan-and-the-things-network): The content on this page is a modified version of what appears in the Sparkfun tutorial. If questions arise, refer to this page!
* The Things Network
## Setup Instructions
1. Download and install the most recent version of the Arduino IDE.
2. Install the ESP Library:
   * Open the Arduino IDE and go to _File_ -> _Preferences_. Check the box next to _Display line numbers_. Copy `https://dl.espressif.com/dl/package_esp32_index.json` and paste it in the field next to _Additional Board Managers URLs_. Click the _OK_ button when finished. [Installation questions?](https://github.com/espressif/arduino-esp32/blob/master/docs/arduino-ide/boards_manager.md)
   * Go to _Tools_ -> _Board: ???_ -> _Board Manager_. Type `esp32` in the field next to _Filter your search_. Click on the option that is named _esp32 by Espressif Systems_ and then press the _Install_ button. Click the _Close_ button when all of the board definitions finish downloading and installing.
3. Install the Sparkfun custom board definitions for the ESP32 LoRa 1-Channel Gateway:
   * Download the [SparkX ESP32 LoRa Arduino Variant Definition (.zip)](https://cdn.sparkfun.com/assets/learn_tutorials/8/0/4/sparkx_esp32_lora-v01.zip) file and save it to the computer. The zip folder will be named _sparkx_esp32_lora-v01.zip_.
   * Unzip the file.
   * Open a new window and navigate to the following location. Replace the three _???_ with the username for the current user. _C:\Users\???\AppData\Local\Arduino15\packages\esp32\hardware\esp32\1.0.0\variants_.
   * Drag the _sparkx_esp32_lora_ folder from the .zip file to the _variants_ folder in the separate window.
   * Go one level up to _C:\Users\???\AppData\Local\Arduino15\packages\esp32\hardware\esp32\1.0.0_. Open _boards.txt_. Copy-and-paste the code below at the bottom of the open file. Save and close the file.
```
##############################################################

sparkx_esp32_lora.name=SparkX ESP32 LoRa Gateway

sparkx_esp32_lora.upload.tool=esptool
sparkx_esp32_lora.upload.maximum_size=1310720
sparkx_esp32_lora.upload.maximum_data_size=294912
sparkx_esp32_lora.upload.wait_for_upload_port=true

sparkx_esp32_lora.serial.disableDTR=true
sparkx_esp32_lora.serial.disableRTS=true

sparkx_esp32_lora.build.mcu=esp32
sparkx_esp32_lora.build.core=esp32
sparkx_esp32_lora.build.variant=sparkx_esp32_lora
sparkx_esp32_lora.build.board=ESP32_DEV

sparkx_esp32_lora.build.f_cpu=240000000L
sparkx_esp32_lora.build.flash_size=4MB
sparkx_esp32_lora.build.flash_freq=40m
sparkx_esp32_lora.build.flash_mode=dio
sparkx_esp32_lora.build.boot=dio
sparkx_esp32_lora.build.partitions=default

sparkx_esp32_lora.menu.PartitionScheme.default=Default
sparkx_esp32_lora.menu.PartitionScheme.default.build.partitions=default
sparkx_esp32_lora.menu.PartitionScheme.minimal=Minimal (2MB FLASH)
sparkx_esp32_lora.menu.PartitionScheme.minimal.build.partitions=minimal
sparkx_esp32_lora.menu.PartitionScheme.no_ota=No OTA (Large APP)
sparkx_esp32_lora.menu.PartitionScheme.no_ota.build.partitions=no_ota
sparkx_esp32_lora.menu.PartitionScheme.no_ota.upload.maximum_size=2097152
sparkx_esp32_lora.menu.PartitionScheme.min_spiffs=Minimal SPIFFS (Large APPS with OTA)
sparkx_esp32_lora.menu.PartitionScheme.min_spiffs.build.partitions=min_spiffs
sparkx_esp32_lora.menu.PartitionScheme.min_spiffs.upload.maximum_size=1966080

sparkx_esp32_lora.menu.FlashMode.qio=QIO
sparkx_esp32_lora.menu.FlashMode.qio.build.flash_mode=dio
sparkx_esp32_lora.menu.FlashMode.qio.build.boot=qio
sparkx_esp32_lora.menu.FlashMode.dio=DIO
sparkx_esp32_lora.menu.FlashMode.dio.build.flash_mode=dio
sparkx_esp32_lora.menu.FlashMode.dio.build.boot=dio
sparkx_esp32_lora.menu.FlashMode.qout=QOUT
sparkx_esp32_lora.menu.FlashMode.qout.build.flash_mode=dout
sparkx_esp32_lora.menu.FlashMode.qout.build.boot=qout
sparkx_esp32_lora.menu.FlashMode.dout=DOUT
sparkx_esp32_lora.menu.FlashMode.dout.build.flash_mode=dout
sparkx_esp32_lora.menu.FlashMode.dout.build.boot=dout

sparkx_esp32_lora.menu.FlashFreq.80=80MHz
sparkx_esp32_lora.menu.FlashFreq.80.build.flash_freq=80m
sparkx_esp32_lora.menu.FlashFreq.40=40MHz
sparkx_esp32_lora.menu.FlashFreq.40.build.flash_freq=40m

sparkx_esp32_lora.menu.FlashSize.4M=4MB (32Mb)
sparkx_esp32_lora.menu.FlashSize.4M.build.flash_size=4MB

sparkx_esp32_lora.menu.UploadSpeed.921600=921600
sparkx_esp32_lora.menu.UploadSpeed.921600.upload.speed=921600
sparkx_esp32_lora.menu.UploadSpeed.115200=115200
sparkx_esp32_lora.menu.UploadSpeed.115200.upload.speed=115200
sparkx_esp32_lora.menu.UploadSpeed.256000.windows=256000
sparkx_esp32_lora.menu.UploadSpeed.256000.upload.speed=256000
sparkx_esp32_lora.menu.UploadSpeed.230400.windows.upload.speed=256000
sparkx_esp32_lora.menu.UploadSpeed.230400=230400
sparkx_esp32_lora.menu.UploadSpeed.230400.upload.speed=230400
sparkx_esp32_lora.menu.UploadSpeed.460800.linux=460800
sparkx_esp32_lora.menu.UploadSpeed.460800.macosx=460800
sparkx_esp32_lora.menu.UploadSpeed.460800.upload.speed=460800
sparkx_esp32_lora.menu.UploadSpeed.512000.windows=512000
sparkx_esp32_lora.menu.UploadSpeed.512000.upload.speed=512000

sparkx_esp32_lora.menu.DebugLevel.none=None
sparkx_esp32_lora.menu.DebugLevel.none.build.code_debug=0
sparkx_esp32_lora.menu.DebugLevel.error=Error
sparkx_esp32_lora.menu.DebugLevel.error.build.code_debug=1
sparkx_esp32_lora.menu.DebugLevel.warn=Warn
sparkx_esp32_lora.menu.DebugLevel.warn.build.code_debug=2
sparkx_esp32_lora.menu.DebugLevel.info=Info
sparkx_esp32_lora.menu.DebugLevel.info.build.code_debug=3
sparkx_esp32_lora.menu.DebugLevel.debug=Debug
sparkx_esp32_lora.menu.DebugLevel.debug.build.code_debug=4
sparkx_esp32_lora.menu.DebugLevel.verbose=Verbose
sparkx_esp32_lora.menu.DebugLevel.verbose.build.code_debug=5
```
   * The _sparkx_esp32_lora-v01.zip_ folder can be deleted as long as the _sparkx_esp32_lora_ folder is inside of the _variants_ folder.
4. Download the .zip folder contians the libraries and sample sketch used to program the gateway. Install the libraries:
   * Download the [ESP-1ch-Gateway-v5.0-master (.zip)](https://github.com/things4u/ESP-1ch-Gateway-v5.0/archive/master.zip) to your computer.
   * Unzip the _ESP-1ch-Gateway-v5.0-master.zip_ file by double clicking on the file. Go to _ESP-1ch-Gateway-v5.0-master_ -> _libraries_.
   * Open a separate window and navigate to _C:\Users\???\Documents\Arduino\libraries_. Replace the three _???_ with the username for the current user.
   * Copy-and-paste all of the folders from the _libraries_ folder in the .zip file to the _libraries_ folder in the separate window at _C:\Users\???\Documents\Arduino\libraries_.
5. Install the _ESP-sc-gway_ sketch:
   * Navigate to _C:\Users\???\ESP-1ch-Gateway-v5.0-master.zip\ESP-1ch-Gateway-v5.0-master_ in the .zip file from the previous step.
   * Open a separate window and navigate to _C:\Users\???\Documents\Arduino_. Replace the three _???_ with the username for the current user. This is the default location for the Sketchbook.
   * Copy-and-paste the _ESP-sc-gway_ folder from the .zip file to the separate window (_C:\Users\???\Documents\Arduino_).
   * The _ESP-1ch-Gateway-v5.0-master.zip_ folder can be deleted.
6. Go to _C:\Users\???\Documents\Arduino\ESP-sc-gway_ and open the _ESP-sc-gway.ino_ file. **Note: There are two files that have this name. Choose the one that has the _.ino_ extension.**
7. Configure the _ESP-sc-gway.h_ tab in the open sketch:
   * Line 46: `#define _LFREQ 915`
   * Line 64: `#define _CAD 0`
   * Line 90: `#define _PIN_OUT 6`
   * Line 138: `#define OLED 0`
   * Line 179: `#define _TTNSERVER "us-west.thethings.network"`
   * Line 195: `#define _DESCRIPTION "CRIFFLE Gateway"`
   * Line 196: `#define _EMAIL "YOUR_EMAIL@gmail.com"`
   * Lines 198-199: Replace the numbers on these two lines with the latitude and longitude for the gateway. _The Things Network_ provides a simple map for finding this information after you create an account (explained in a future step).
   * Lines 261-265: Change the code on these lines as follows:
```
wpas wpa[] = {
	{ "" , "" },							// Reserved for WiFi Manager
	{ "WIFI_NETWORK_SSID", "YOUR_WIFI_PASSWORD" }
};
```
8. Something


* Download the sketch examples and libraries- see Sparkfun tutorial
* Copy libraries in the download to the Libraries folder in documents
* Copy ESP-sc-gway folder from the download to the Sketch folder in documents
* Open ESP-sc-gway; change .ino name to match the root folder if you make a copy
* Create account on the things network
* Make changes to esp-sc-gway.h: us.pool.ntp.org, ntp_timezone -4
* Make changes to loraModem.h- see Sparkfun tutorial
* Change board and port
* Compile and upload sketch
* Open serial monitor and change baud rate to 115200
* It took a couple of uploads for it to work.
* Set static ip
* Find ip and load in browser
