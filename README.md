# ESP-Lamp

A simple lamp design inspired by Xiaomi - [Thingiverse](https://www.thingiverse.com/thing:6421767), [Printables](https://www.printables.com/model/762873-esp-lamp-led-xiaomi-inspired-lamp)

Included is the ESPHome code is used to control the lamp with the rotary encoder and via Home Assistant.

## ESPHOME

The code functions as such...

* A single press will toggle the LED light, it will resume whatever the last brightness setting was
* A double, triple, quad or hold press sends a unique event each to Home Assistant, this can then be used in Automations to control anything else.
* Turning the dial will increase or decrease the brightness only if the light is turned on.
  * If you try to increase the brightness past 100%, the light will flash to tell you it's at max brightness. and vice versa with the minimum brightness
 
## WLED

If you’re considering using WLED, Follow the instructions here for the rotary encoder - https://mm.kno.wled.ge/usermods/Rotary-Encoder. I lean towards ESPHome, but I initially tested WLED. Unfortunately, I encountered issues with the rotary encoder functionality but you may be able to get this to work as it is supported.
