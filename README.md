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
2. Open the Arduino IDE and go to _File_ -> _Preferences_. Check the box next to _Display line numbers_. Copy `https://dl.espressif.com/dl/package_esp32_index.json` and paste it in the field next to _Additional Board Managers URLs_. Click the _OK_ button when finished. [Installation questions?](https://github.com/espressif/arduino-esp32/blob/master/docs/arduino-ide/boards_manager.md)
3. Go to _Tools_ -> _Board: ???_ -> _Board Manager_. Type `ESP32` in the field next to _Filter your search_. Click on the option that is named _esp32 by Espressif Systems_ and then press the _Install_ button. Click the _X_ in the upper right corner when all of the board definitions finish downloading.
* Solder header pins
* Install the ESP32 library https://github.com/espressif/arduino-esp32/blob/master/docs/arduino-ide/boards_manager.md
* Install ESP32 through board manager; update boards and managers by going to board manager -> Type -> Updateable 
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
