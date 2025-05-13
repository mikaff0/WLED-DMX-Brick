# WLED-DMX-Brick
I Build this brick with an DMX In and Out and an ESP32-S3 with WLED in the middle.
The use case is to put it in a DMX line, and have an automatic scene on boot and a simplified UI for controlling the Lamps but it is always possible to control the Lamps by the central DMX-Master for the bigger events in the house.


I used:
- ESP32-S3 Mini / Zero
- SN75176
- Neutrik XLR 
- NC3FAAH
- NC3MAAH

All in a 3D printed box. https://www.printables.com/model/1100733-dmx-wled-brick

![alt text](/Images/20241207_210559.jpg)

## Detailed guilding guide:


### Flash the ESP32-S3:

You can flash it with https://wled-compile.github.io/.
You can load my configuration from the file 'WLED_compile_DMX-Brick.json'.

1. Start the build and flash the ESP.
2. Build the 'Brick':
3. Print the case from printables.
4. I connect all components with thin enameled wire but you also can use other wires.

### Connection scheme:
![alt text](/Images/WLED-DMX-Brick-Rev0_Schaltplan.jpg)

### Configure the WLED instance:
1. The config of the data pin to the transceiver is hardcoded to pin 2
2. Config the pin to the DE pin of the transceiver as the LED Relay or an LED Switch (in my schematic pin 3).
3. Config the DMX Chanels as you preferre.
4.Adding some LEDs, wich has the chanels of your DMX Chanel Config.
5. Notice that WLED is realy limited with the DMX settings.
6. Further informations on https://kno.wled.ge/interfaces/dmx-output/ .
