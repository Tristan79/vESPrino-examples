###What is the vESPrino-dongle?
Essentially this is an ESP8266-based board that has several improvement that make it more suitable for productive projects than other boards
* USB-2-Serial module - so that no additional hardware is require to program it
* Convenient button tied to GPIO0 and pulled-up by default
* WS2812B LED tied to GPIO2 (so that driving via NeoEsp8266Uart800KbpsMethod is possible)
* Deep-sleep mode enabled by default with GPIO16 connected to RST
* Auto-Programming circuit uses CH_PD pin instead of RST (compared to other clones), which makes it a bit more reliable
* Mounting holes - so that the device can be easily integrated into enclosures
* 9 pins broken out - just the most important ones - to reduce soldering time
* Naming of the pins follows the NodeMCU and wemosCC convention as one of the most popular on the market
* Male USB Port (optional) - so that you can directly plug it into the PC
* MOSFET 3A, connected to GPIO 15 and 5V - so that high-power external devices can be controlled 
* Broken-out pins are sorted in a way that some sensors can be directly plugged (SI7021, BME280, TSL2561 and others)

###Getting Started
1. Install drivers as described here: http://vair-monitor.com/drivers/
2. Install the latest version of Arduino from here (any above 1.6.8 will work): https://www.arduino.cc/en/Main/Software
3. Install the ESP8266 Development Kit for Arduino as described here: https://github.com/esp8266/Arduino
4. Configure your board as NodeMCU v0.9 or v1.0 (then the pin names like D1, D5 will work). For upload speed you can set 256000 baud as it works quite stable. On higher speeds it also works but not so consistently and may occasionally not be able to switch the device to programming mode
5. Clone or download this repository. If you already have a previous installation you can copy the sketches to your sketches directory and the "libraries" directory to your libraries. Just pay attention to the NeoPixelLibrary - if you have an older version - the examples may not work

###Examples
* [vESPrino_Blink](https://github.com/vlast3k/vESPrino-examples/tree/master/vESPrino_Blink) - The Hello vESPrino! example. Utilizes the RGB Led and blinks it in Red, Green, Blue colors
* [vESPrino_Blink](https://github.com/vlast3k/vESPrino-examples/tree/master/vESPrino_LED_Button) - A more advanced example which combines usage of the Button and LED. Clicking the Button changes the color of the led and clicking&holding it - changes the intensity. Feel free to modify it for more interesting stuff
* ESP8266 Examples - For examples related to setting up WiFi and other core functionalities of the ESP - they are accessible from the Arduino IDE: Menu->Examples->ESP**** stuff - usually you just need to change your WiFi accesspoint name and they work
* More examples - I am still catching up with documentation and examples. Soon i will post more examples of interacting with the different sensors

