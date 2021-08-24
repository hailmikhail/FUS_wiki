[Back to Readme](https://github.com/Kvitekvist/FUS/blob/main/README.md)

# Install Microsoft Visual C++ Redistributable Package

We doubt you need to do this since you likely already have this installed, but better safe than sorry. The package is required for MO2 and you can download it from [Microsoft](https://support.microsoft.com/en-us/help/2977003/the-latest-supported-visual-c-downloads). Download the x64 version under "Visual Studio 2015, 2017 and 2019". [Direct link](https://aka.ms/vs/16/release/vc_redist.x64.exe) if you can't find it.

# Steam Config

First of all, we highly recommend not using any supersampling, neither in Steam/Oculus, nor ingame. Set the render resolution to 100% (or 1.0 in Oculus) everywhere. Supersampling is a very inefficient way of anti-aliasing and given the hunger for performance in Skyrim VR you most likely will drop into reprojection when you try using it. 

## Disable the Steam Overlay

The Steam Overlay can cause issues with ENB and is recommended to be turned off.

Open the Properties window (right click the game in your Library->Properties), navigate to the _General_ tab and un-tick the _Enable the Steam Overlay while in-game_ checkbox. This can be done even when the game is not yet installed.

## Set the game language to English

Just do it. This entire Modlist is in English and 99% of all mods you will find are also in English. We highly recommend playing the game in English and **will not give support to people with a non-English game**. Wabbajack does not support SkyrimVR files in other languages either. Wabbajack will fail file validation for other languages.

Open the Steam Properties window, navigate to the _Language_ tab and select _English_ from the dropdown menu.

## Clean Skyrim

You can skip this step if you did not install Skyrim VR yet.

Delete the following directories:
1. Open Stem Steam
2. Right click on “Skyrim VR”
3. Choose: Properties >>  Local Files >>  Browse

![image](https://i.ibb.co/V33zFWt/steam-folder.png)

4. Delete all content in the folder. Do not reinstall yet.
5. Open Windows Search and copy/paste %LOCALAPPDATA%
6. Delete the Skyrim VR folder
7. Navigate to Users\YOURNAME\Documents\My Games\
8. Delete the SkyrimVR folder

## Install Skyrim

Open Steam and ensure that Skyrim is uninstalled through on it. Otherwise, go up one step and clean it.

Then, just install Skyrim VR from Steam.

## Start Skyrim

After you have done everything above and got a clean Skyrim VR installation ready, start the Launcher and and let it do the initial graphics check. Do not worry about this part as the installation will replace this graphics settings.
Start the game and exit once you're in the main menu. This will make sure that some of the tools the Mod Organizer that comes with FUS will find the Skyrim VR folder.

# Install Wabbajack

Grab the latest release of Wabbajack from [here](https://www.wabbajack.org/#/) and place the `Wabbajack.exe` file in a _working folder_. This folder **must not** be in a _common folders_ like your Desktop, Downloads or Program Files folder. It's best to create a Wabbajack folder near the root level of your drive like `C:/Wabbajack`.
