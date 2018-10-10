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
  * Download the [SparkX ESP32 LoRa Arduino Variant Definition (.zip)](https://cdn.sparkfun.com/assets/learn_tutorials/8/0/4/sparkx_esp32_lora-v01.zip) file and save it to the computer.
  * Something else
4. Something
* Add custom board- see Sparkfun tutorial; The pathway is C:\Users\???\AppData\Local\Arduino15\packages\esp32\hardware\esp32\1.0.0\variants
* Add board to boards.txt- see Sparkfun tutorial; The pathway is C:\Users\???\AppData\Local\Arduino15\packages\esp32\hardware\esp32\1.0.0
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
