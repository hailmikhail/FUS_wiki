[Back to Readme](https://github.com/Kvitekvist/FUS/blob/main/README.md)

# Activate the Essential Files

This step will add the required files for SKSE, Engine Fixes, DLL loader and other essential files that cannot be handled by MO2.

DO NOT RUN LOOT! Everytime you run LOOT a kitten dies and we cry in the corner. The load order is exactly as it should be, do not change it.

First, run the program named Essentials Files from Mod Organizer 2.

![image](https://i.ibb.co/KrvCB09/essentials1.jpg)

Then Click "OK" if you get a message saying something about "Failed to check for update". This is ok.

![image](https://i.ibb.co/P5mpMfH/enb2.jpg)

Then navigate to the Presets menu by pressing the symbol in the top left (the three lines). The menu should look like this:

![image](https://i.ibb.co/YkFSZJ1/enb3.jpg)

Then you will see this menu and need to first disable all, and then enable like this:

![image](https://github.com/Kvitekvist/FUS/blob/main/images/essential_files_steam.png?raw=true)

If any options are already checked, then you should first uncheck them (grey) then check the essential files you need. If you switch options it is automatically synched, but using the synch button does not hurt either.

1. You must activate the "00 Essential Files" option. 
2. SteamVR - Necessary if you run the game via SteamVR.
3. opencompoisite - This can replace SteamVR and will give Oculus users a strong performance boost. _Switch off the `01 steamVR` option in that case!_ They replace each other.
4. openvr_fsr - AMD sharpener, not compatible with opencomposite, mixed reviews. Test at your own risk.
5. update skyrim.ini - will only update that specific ini named skyrim.ini in the steam\skyrimvr folder. You must toggle this option off and then on to get the update. This has to be done once after installing FUS! The other inis need to be updated separately if you are coming from an older version with changed in settings (assuming you even want to change the inis).