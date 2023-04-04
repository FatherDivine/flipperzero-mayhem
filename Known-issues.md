# Mode switch

The firmware on the ESP32 [switches mode](Firmware-mode) powering the 5V rail in the Flipper Zero, and since when is plugged to USB 5V output is always enabled this might interfere how the apps behave. If you have any issue, please disconnect the board from USB and test again. You can also press reset on the ESP32 while switching to another Flipper Zero fap to switch mode. This could be fixed in the future.

# 3V3 rail

Optionally, you could power the ESP32 via 3V3. This requires [to cut the 5V trace](PCB-and-pinout) in the PCB and put a solder joint on the pad that says 3V3. However, this is not recommended because the ESP32 might use more power than what the Flipper Zero can provide and produce problems. This is a limitation of the Flipper, and cannot be fixed.

Consider this if you really want to use the 3V3 instead of 5V.

# ESP32CAM extra GND

**Note:** This does not apply to newer PCBs (from Mayhem v1.2), check if your PCB says N/A. Consider this only if you are making a DIY version.

Some cameras have 3 GND pads (the original design) but others have reconnected that pin to something else, this interferes with the boot of the ESP32 if this pin is grounded. With a multitester, check if all the pads with the label GND are connected between them to isolate the problem.

![image](https://user-images.githubusercontent.com/1091420/220142269-1fa92681-601c-48aa-b9fa-d29079979f27.png)
