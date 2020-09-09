# Lortinchen

Lortinchen is a small PCB combining an ESP8266 with an RFM96 for Lora Communication. We use this as a Wifi location tracker in our OpenBike project to track our Bikes.

![](./images/lortinchen-top.jpg)

## Flash firmware

To flash firmware before soldering the ESP on the PCB, you can use an *ESP-12 test board fixture programmer*. So you don't need to solder a connection to a Serial-USB-Adapter and don't need the flash and reset buttons.

If you want to update or flash firmware after soldering, you need the 1K resistors and the flash and reset  buttons. Then solder GND, RX, TX and 3V to your Serial-USB-Connector. To go into flash-mode hold flash button, press reset, then release flash button. Now you can flash the firmware from PlatformIO.

## Parts

### Required

 * ESP8266 Modules (ESP-12E or ESP-12F with on board PCB antenna or ESP-07 or ESP-07S for external antennas)
 * RFM96
 * 5x 10K 0603 resistors
 * 1x 100uF (107C/6032) capacitor

### Optional

 * 2x 1K 0603 resistors (for serial connection and flashing after soldering)
 * 2x SMD 2Pin 3X4 mm tactile buttons (for easy flashing and resetting after soldering)
 * 1x AMS111733 LDO (only if power supply is more than 3,3V, but will consume more power.)
 * 1x 680K and 1x 100K 0603 resistor (for voltage devider), now supported in the firmware to mesure voltage. If you don't use the AMS111733, connect the 12V and the 3V Pin to mesure voltage.


## Power supply

The Board can be powered by two AA (LR6) batteries on the 3V3 pad, without the AMS111733 installed. Our first test-devices are running now for around 4 months without changing batteries.
