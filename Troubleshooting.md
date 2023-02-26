# Troubleshooting

For general troubleshooting, uploading the firmware from Arduino IDE, check this video:

[![Troubleshooting](https://img.youtube.com/vi/Gld-tHnGydA/0.jpg)](https://www.youtube.com/watch?v=Gld-tHnGydA)

## The Flipper apps, faps do not run

You may need to [compile the fap files](wiki/Compilation-of-the-faps) for your firmware. The provided fap files are intended to be used with the unleashed firmware (usually the latest release).

The differences in firmwares, make the fap files not fully portables.

## The apps are not talking with the ESP32

If you can open the faps, but it seems nothing works, then you should investigate with a serial monitor (as shown in the video on top of this page). Connect the Flipper Zero to your computer and open [_GPIO/USB-UART bridge_](Compilation-of-the-firmware#flipper-zero). Open the serial monitor to the port of the Flipper Zero (for example the monitor on Arduino IDE). Reset the ESP32 and read the messages, you might need to change the bauds:

* **ESP32 boot**: 115200 bauds is common for the boot messages. If there is a bootloop, you need to play with the [board options](Compilation-of-the-firmware#board-settings).

A boot loop with output constantly debug text while rebooting the board, similar to:

    rst:0x1 (POWERON_RESET),boot:0x33 (SPI_FAST_FLASH_BOOT)
    configsip: 0, SPIWP:0xee
    clk_drv:0x00,q_drv:0x00,d_drv:0x00,cs0_drv:0x00,hd_drv:0x00,wp_drv:0x00
    mode:DIO, clock div:2
    load:0x3fff0030,len:1184
    load:0x40078000,len:13104
    load:0x40080400,len:3036
    entry 0x400805e4
    Guru Meditation Error: Core  1 panic'ed (IllegalInstruction). Exception was unhandled.
    Memory dump at 0x400ff4fc: 4eca3104 4e84082c 00a88c88
    Guru Meditation Error: Core  1 panic'ed (IllegalInstruction). Exception was unhandled.
    ...

* **ESP32 firmware**: 230400 bauds is common for the firmware. You can read what the firmware is printing. It might take a second after the boot.

## The apps do not switch mode in the ESP32 correctly

Please disconnect the Flipper USB cable while using the apps as commented in the [known issues](Known-issues#mode-switch). 

## The ESP32 does not output any serial messages, nor it is able to be programmed, seems to be dead

You might have an unit with a different pinout, check the [known issues](Known-issues#esp32cam-extra-gnd).