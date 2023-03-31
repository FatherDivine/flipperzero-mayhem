This is a simple app that exposes the stream of the camera in a new AP from the ESP32.

Start the app, connect to the new WiFi AP displayed on the screen and open the address on the screen from your phone or computer to see the raw stream from the camera. You can use tools like OBS or VLC to manipulate the incoming stream (or record it).

![image](https://user-images.githubusercontent.com/1091420/229062076-8670968b-32df-45d2-8792-121691435b8c.png)

If you can't connect, check:

* That you are actually connected to the WiFi AP. Some devices may switch to another AP if the one you recently connected does not has internet access (as is with this AP).

* Check that you are actually opening the address as `http://<address>`, not searching for the address. Also if your device has multiple network sources (i.e. _LAN/cellular_) find a way to make it use the correct network to find the ESP32.

The idea is to extend this app, for example you could add functionality to the page, take photos, change parameter of the camera. Check the source code and contribute.