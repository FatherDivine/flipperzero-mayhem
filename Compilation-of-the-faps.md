You need to fork a Flipper Zero firmware for this step. I will use [DarkFlippers/unleashed-firmware](https://github.com/DarkFlippers/unleashed-firmware).

1. Download (and unpack) the .zip or clone [DarkFlippers/unleashed-firmware](https://github.com/DarkFlippers/unleashed-firmware)

2. Copy the applications from [flipper_companion_apps/applications/plugins](https://github.com/eried/flipperzero-mayhem/tree/master/flipper_companion_apps/applications/plugins) to `unleashed-firmware\applications\plugins` from the previous step

> I use _Junction links_ to work on the apps in a different place, but any method like this is up to you
> ![image](https://user-images.githubusercontent.com/1091420/220391415-65dba323-e729-4d03-8f41-5fbedd42ea6a.png)

3. Open with VS Code or a similar editor

3. Execute `./fbt faps` on a new terminal in VS Code. If the compilation goes OK, the .faps will be on the directory `build\*-firmware-*\.extapps` from the step one