[Back to Readme](https://github.com/Kvitekvist/FUS/blob/main/README.md)

# Activate the Essential Files

This step will add the required files for SKSE, Engine Fixes, DLL loader and other essential files that cannot be handled by MO2.

DO NOT RUN LOOT! Everytime you run LOOT a kitten dies and we cry in the corner. The load order is exactly as it should be, do not change it.

First, run the program named Essentials Files from Mod Organizer 2.
If you don't find the Essentials Files in the dropdown, then Wabbajack did not install successfully. Re-run wabbajack and pay attention to errors during install.

![image](https://github.com/Kvitekvist/FUS/blob/main/images/essential%20files.jpg)

Then Click "OK" if you get a message saying something about "Failed to check for update". This is ok.

![image](https://i.ibb.co/P5mpMfH/enb2.jpg)

Then navigate to the Presets menu by pressing the symbol in the top left (the three lines). The menu should look like this:

![image](https://i.ibb.co/YkFSZJ1/enb3.jpg)

Then you will see this menu and need to first disable all, and then enable like this:

![image](https://github.com/Kvitekvist/FUS/blob/main/images/essential_files_steam.png?raw=true)

If any options are already checked, then you should first uncheck them (grey) then check the essential files you need. 

Always press the `Synch` button after you change options!

* You must activate the "Essential Files" option. 

### **ALL OTHER OPTIONS ARE OPTIONAL**

* SteamVR - Vanilla SteamVR options, this is the default `openvr_api.dll` file without manipulations.
* OpenComposite - This replaces the SteamVR default `openvr_api.dll` and will give Oculus users a strong performance boost. __FIRST__ _switch off the SteamVR option in that case!_ The files replace each other. IMPORTANT: This will break `Virtual Desktop`, `VR FPS Stabilizer` and `Mage VR`, but the performance boost is worth it for most users.
* OpenVR Fixed Foveated Rendering - This also replaces the `openvr_api.dll` file and is thus incompatible with the others. It enables fixed foveated rendering. See the [original page](https://github.com/fholger/openvr_foveated/) for explanations. It does give a slight flicker in the very edges, but you can adjust the rings in the configuration file of FFR to tweak it until you are happy with it. If you change the stuff best change it directly in the Skyrim VR base game folder and make a backup so in case it gets overwritten by a new FUS update you can use your settings again. The defaults we provide are giving a slight performance improvement while having almost no impact on the visuals (we also disabled the Nvidia sharpener because CAS is better in our case), hence we recommend using it. If you find it too annoying either make the rings even larger or just use the default SteamVR option.
* OpenVR FSR - AMD sharpener, not compatible with OpenComposite, mixed reviews. Test at your own risk.
* Real Virtual Magic Libraries - This is needed only if you use the Real Virtual Magic brain-computer interface mod by Cangar.

Always press the `Synch` button after you change options!