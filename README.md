# LoRa-CRIFFLE
Instructions and code for building the LoRa version of the CRIFFLE.
## Gateway
* Use https://learn.sparkfun.com/tutorials/esp32-lora-1-ch-gateway-lorawan-and-the-things-network?_ga=2.47104423.1200190544.1539095630-844852618.1539095630&_gac=1.205334180.1539096507.EAIaIQobChMI_6y2ns353QIVyV6GCh3GHAEjEAAYASAAEgKzjPD_BwE
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
