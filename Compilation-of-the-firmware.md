You need to install the board following this [instructions](https://github.com/espressif/esp32-camera). Open `flipperzero-mayhem/esp32cam_marauder/esp32cam_marauder.ino` in Arduino IDE and compile it normally. 

## Required libraries

You need the libraries listed on [esp32cam_marauder/libraries](https://github.com/eried/flipperzero-mayhem/tree/master/esp32cam_marauder/libraries)

## Board settings
![image](https://user-images.githubusercontent.com/1091420/220386857-d7d21b88-f7d5-4e67-a78f-b91f3ed198b5.png)

For some boards, the _Flash Mode_ should be **DIO**.

# Upload

The ESP32CAM needs to be manually put on upload mode. Check [First-steps#firmware-update](First-steps#firmware-update).

## Flipper Zero

Go to GPIO and select USB-UART Bridge. The default settings are ok. This enables 5V on GPIO automatically, so no need to do anything else.

![image](https://user-images.githubusercontent.com/1091420/220390026-140cccf8-e9af-46ef-9ba3-327d29363bf9.png)

## Serial-USB adaptor

Connect RX, TX, GND and PWR (5V to VCC OR 3V3 to 3V depending on your adaptor)

