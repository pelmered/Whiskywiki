Many games will work out of the box, but some are more tricky. Things that frequently cause issues with Wine are 3rd party launchers, anti-cheats, and online services. Some of these games have workarounds, and some do not.

## Elden Ring
- Create a new Windows 10 bottle
- Install in Steam as normal
- In Whisky, find `elden_ring.exe` in the Program list and press `Show in Finder`
- Rename `start_protected_game.exe` to something else, and rename `elden_ring.exe` to `start_protected_game.exe`
  > **Note**\
  > This will disable online play features
- Start Elden Ring from Steam as normal

## Diablo IV
- Create a new Windows 10 bottle
- Go to Config
  - Change Windows Version to 19042 (Make sure to press enter to submit the change)
  - Enable ESync
- Install Battle.net
- On the Battle.net login screen, press the cog icon in the top right. Click on `Advanced`, and disable `Use hardware acceleration when available`
- Go back to Whisky. Click on `File` > `Kill All Bottles`
- Restart Battle.net
- Login and install Diablo IV as normal

## Star Wars Jedi: Fallen Order
- Create a new Windows 10 bottle
- Install in Steam as normal
- In Whisky, find `SwGame-Win64-Shipping.exe` in the Program list and run it

## Horizon Zero Dawn
- Create a new Windows 10 Bottle
- Install Horizon Zero Dawn as normal
- On your bottle click `Config` then `Open Registry Editor`
- Navigate to `HKEY_LOCAL_MACHINE > Hardware > Description > System > CentralProcessor > 0`
- Double-click to edit the `~MHz` key
- Change the base to `Decimal` and type the value `1100`
- Press `OK` then close the Registry Editor
- Start Horizon Zero Dawn as normal

## Skyrim SE
- Create a new Windows 10 bottle
- Install in Steam as normal
- In Whisky, find `SkyrimSELauncher.exe` in the Program list and press `Show in Finder`
- Rename `SkyrimSELauncher.exe` to something else, and rename `SkyrimSE.exe` to `SkyrimSELauncher.exe`
- On your bottle click `Winetricks...`
- Run the following command `dotnet48 vcrun2019 dxvk1103 d3dx11_43 d3dcompiler_43 d3dcompiler_47 faudio`
  > **Note**\
  > This WILL require user interaction and will likely take a rather long time to complete
- Start Skyrime from Steam as normal

## Elite Dangerous - NOT WORKING
- Install winetricks\
  `brew install winetricks`
- Create a new Windows 10 bottle
- Run the following winetricks command\
  `arial corefonts cjkfonts vcrun2019 d3dcompiler_43 d3dcompiler_47 d3dx9 ie8 dotnet452 win10`
  > **Note**\
  > This WILL require user interaction and will likely take a rather long time to complete
- Install Steam
- Install Elite Dangerous
- Run Elite Dangerous *from Steam*.
  > **Warning**\
  > You will be unable to log in if you do not launch from Steam