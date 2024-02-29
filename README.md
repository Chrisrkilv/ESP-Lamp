# ESP-Lamp

A simple lamp design inspired by Xiaomi - [Thingiverse](https://www.thingiverse.com/thing:6421767), [Printables](https://www.printables.com/model/762873-esp-lamp-led-xiaomi-inspired-lamp)

Included is the ESPHome code is used to control the lamp with the rotary encoder and via Home Assistant.

## Parts & Wiring
Rotary Encoder with Click - https://amzn.to/48lDSXV
ESP32 Module (I used ESP32-C3-Supermini) - https://amzn.to/3vsUU7Z
M2, M3 & M4 Screws, Washers & Nuts - https://amzn.to/3TObHfK
20mm Metal Washer (Can be printed but not recommended)
WS2811/WS2812/WS2812B or WS2813 (1 Meter 5V) LED Strip - https://amzn.to/3Havtuk
USB-C Female Ports - https://amzn.to/3TJWYT8
10mm rubber feet (Or print in TPU) - https://amzn.to/3S9bQZY
Spare 1m cable with at least 3 Internal wires (I used an old USB cable).
Other spare wires for general wiring of components
USB-C to USB-A Cable
USB-A power brick (at least 1.5A)

See the wiring diagram for detailed overview, full assembly and wiring instructions exist on thingiverse & printables. The Lamp includes an ESP32-C3-Supermini but any ESP32, ESP8266 device can be used for this project as long as it can run ESPHome or WLED.

## ESPHOME

The code functions as such...

* A single press will toggle the LED light, it will resume whatever the last brightness setting was
* A double, triple, quad or hold press sends a unique event each to Home Assistant, this can then be used in Automations to control anything else.
* Turning the dial will increase or decrease the brightness only if the light is turned on.
  * If you try to increase the brightness past 100%, the light will flash to tell you it's at max brightness. and vice versa with the minimum brightness
 
## WLED

If you’re considering using WLED, Follow the instructions here for the rotary encoder - https://mm.kno.wled.ge/usermods/Rotary-Encoder. I lean towards ESPHome, but I initially tested WLED. Unfortunately, I encountered issues with the rotary encoder functionality but you may be able to get this to work as it is supported.
