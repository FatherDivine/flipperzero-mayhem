If the camera is not connected, you should lift the plastic tab on the ESP32CAM board, and slide the camera flat cable as show below:
![image](https://user-images.githubusercontent.com/1091420/220083851-cf85147a-3890-43d9-a3cf-b954190847e1.png)

You can use the electronic components as a guide how deep you should set the connector before pressing the plastic tab down to lock the camera in place:

![image](https://user-images.githubusercontent.com/1091420/220084163-56ceb266-47a0-4e5b-be3f-5b908d7cd519.png)

It is a good idea to add a piece of double side tape and secure the camera so it does not dangle. 

If you ever need to upload the firmware to the ESP32, you need to remember that you need to short IO0 and GND while pressing the reset button that is on the back of the ESP32. An easy way to do this is to place a pen with a metallic tip between those pins:

![image](https://user-images.githubusercontent.com/1091420/220084674-29188dca-d82f-4003-addf-233cfe5e2c14.png)
