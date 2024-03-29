[Back to Readme](https://github.com/Kvitekvist/FUS/blob/main/README.md)

# Install Microsoft Visual C++ Redistributable Package

We doubt you need to do this since you likely already have this installed, but better safe than sorry. The package is required for MO2 and you can download it from [Microsoft](https://support.microsoft.com/en-us/help/2977003/the-latest-supported-visual-c-downloads). Download the x64 version under "Visual Studio 2015, 2017 and 2019". [Direct link](https://aka.ms/vs/16/release/vc_redist.x64.exe) if you can't find it.

# Install .NET version 8.0
Please ensure you have .NET v8.0 installed. Download the desktop app x64 AND the console app x64 versions from Microsoft here: https://dotnet.microsoft.com/en-us/download/dotnet/8.0/runtime

# Steam Config

First of all, we recommend **not using any supersampling**, neither in Steam/Oculus, nor ingame. Set the render resolution to 100% (or 1.0 in Oculus) everywhere (in SteamVR remember to *definitely check* both the global video settings as well as the game specific settings so that they are at 100%). Supersampling is a very inefficient way of anti-aliasing and given the hunger for performance in Skyrim VR you most likely will drop into reprojection when you try using it. If you really think you need it, be advised that it costs you.

If you come to the discord and complain about performance and we find out you did use more than 100% render resolution we will shame you.

## Disable the Steam Overlay

The Steam Overlay can cause issues with ENB and is **sometimes** recommended to be turned off. However, these issues are rare (personally I never experience any) and disabling the Steam overlay means **you don't get achievements** which are enabled by the engine fixes mod. You can decide yourself which option you find more important.

If you want to disable the overlay, open the Properties window (right-click the game in your Library->Properties), navigate to the _General_ tab and un-tick the _Enable the Steam Overlay while in-game_ checkbox. This can be done even when the game is not yet installed.

Again, in this case, you will not be able to get achievements.

## Set the game language to English

Just do it. This entire modlist is in English and 99% of all mods you will find are also in English. We highly recommend playing the game in English and **will not give support to people with a non-English game**. Wabbajack does not support SkyrimVR files in other languages either. Wabbajack will fail file validation for other languages.

Open the Steam Properties window, navigate to the _Language_ tab and select _English_ from the dropdown menu.

## Clean Skyrim

You can skip this step if you did not install Skyrim VR yet.

Delete the following directories:
1. Open Stem Steam
2. Right click on “Skyrim VR”
3. Choose: Properties >>  Local Files >>  Browse

![image](https://i.ibb.co/V33zFWt/steam-folder.png)

4. While leaving the explorer window open, uninstall the game through steam.
5. Delete all leftover content in the folder. Do not reinstall yet.
6. Open Windows Search and copy/paste %LOCALAPPDATA%
7. Delete the Skyrim VR folder
8. Navigate to Users\YOURNAME\Documents\My Games\
9. Delete the SkyrimVR folder

## Install Skyrim

Open Steam and ensure that Skyrim is uninstalled through on it. Otherwise, go up one step and clean it.

Then, just install Skyrim VR from Steam. Install it to a library in a _working folder_. This folder **must not** be in a _common folders_ like your Desktop, Downloads, or Program Files folder. It's best to create a Steam library folder near the root level of your drive like `C:\SteamLibrary`. 

You should be fine if you follow [this guide on how to create a Steam Library folder elsewhere](https://help.steampowered.com/en/faqs/view/4BD4-4528-6B2E-8327). You only need to follow the “How do I change the default installation path for my games?” section.

If you only have one drive and Steam does not allow having a second library on C: you can use [this tool](https://github.com/LostDragonist/steam-library-setup-tool/wiki/Usage-Guide) to add additional library folders to Steam.

You do not need to set the new folder to the default install location. You can if you would like. Simply having a new location is enough.

After you have a new Steam Library folder outside of the `Program Files (x86)` location, you can install your Skyrim version. When you click to install now you should get a pop-up with a drop-down box in which you can select where you would like to install the game. Simply select the newly created folder from this menu.

## Start Skyrim

After you have done everything above and got a clean Skyrim VR installation ready, start the Launcher and and let it do the initial graphics check. Do not worry about this part as the installation will replace this graphics settings.
Start the game and exit once you're in the main menu. This will make sure that some of the tools the Mod Organizer that comes with FUS will find the Skyrim VR folder.

# Install Wabbajack

Grab the latest release of Wabbajack from [here](https://www.wabbajack.org/#/) and place the `Wabbajack.exe` file in a _working folder_. This folder **must not** be in a _common folders_ like your Desktop, Downloads, or Program Files folder. It's best to create a Wabbajack folder near the root level of your drive like `C:\Wabbajack`. Then run the executable. Windows will complain, but Wabbajack is a trusted open-source project, you need to press "more information" and then "run anyways".
