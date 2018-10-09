# LoRa-CRIFFLE
Instructions and code for building the LoRa version of the CRIFFLE.
## Gateway
* Use https://learn.sparkfun.com/tutorials/esp32-lora-1-ch-gateway-lorawan-and-the-things-network?_ga=2.47104423.1200190544.1539095630-844852618.1539095630&_gac=1.205334180.1539096507.EAIaIQobChMI_6y2ns353QIVyV6GCh3GHAEjEAAYASAAEgKzjPD_BwE
* Solder header pins
* Install the ESP32 library https://github.com/espressif/arduino-esp32/blob/master/docs/arduino-ide/boards_manager.md
* Install ESP32 through board manager; update boards and managers by going to board manager -> Type -> Updateable 
* Add custom board- see Sparkfun tutorial; The pathway is C:\Users\???\AppData\Local\Arduino15\packages\esp32\hardware\esp32\1.0.0\variants
* Add board to boards.txt- see Sparkfun tutorial; The pathway is C:\Users\???\AppData\Local\Arduino15\packages\esp32\hardware\esp32\1.0.0
* Download the sketch examples and libraries- see Sparkfun tutorial; the files go in the libraries folder
*Make changes to esp-sc-gway.h using Geany; Spread should be SF10-12, CAD 0
