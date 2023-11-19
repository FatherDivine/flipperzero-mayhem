You need to fork a Flipper Zero firmware for this step. I will use [Xtreme-Firmware](https://github.com/Flipper-XFW/Xtreme-Firmware).

1. Download (and unpack) the .zip or clone the Flipper Zero firmware repository

2. Copy the applications from [flipper_companion_apps/applications/](https://github.com/eried/flipperzero-mayhem/tree/master/flipper_companion_apps/applications) to `applications/external`

> If you plan to compile the apps many times, you can use _Junction links_ to work on the apps in a different place and keep only the link in `applications/external` while keeping the source code of the applications on another location 

> ![image](https://user-images.githubusercontent.com/1091420/220391415-65dba323-e729-4d03-8f41-5fbedd42ea6a.png)

3. Open with VS Code or a similar editor

3. Execute `./fbt faps` on a new terminal in VS Code. If the compilation goes OK, the .faps will be in a subfolder on the directory `build`