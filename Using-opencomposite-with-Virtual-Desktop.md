# Opencomposite with Virtual Desktop
It is now possible to use opencomposite for all users, and it is compatible with Virtual Desktop. To get this working, you will need to check ceretain steps. Here we will list known methods to get these to work. If you are not using a Meta / Oculus device, just skip those steps refering to the Oculus app.

## Method 1 - Set all openxr runtimes to steamvr
There are quite a few places that openxr settings are applied. Follow these steps to set it all up.

### Step 1 - Openxr in Virtual Desktop Streamer on the desktop PC.
![](https://github.com/Kvitekvist/FUS/blob/main/images/VD%20Steamvr.jpg?raw=true)

Open the Virtual Desktop Streamer and go to Options.
In the OpenXR Runtime, choose "SteamVR" from the dropdown list.
This was verified on version 1.29.8 of Virtual Desktop Streamer (non-steam version. I used the one from the website). No beta version required.

### Step 2 - Verify Openxr in Oculus App on the desktop PC
![](https://github.com/Kvitekvist/FUS/blob/main/images/oculus%20steamvr.jpg?raw=true)

Open up the Oculus app, and go to settings.
From Settings, go to the "General" tab.
Here you will find "Openxr runtime". Make sure it says "Current OpenXR Runtime: SteamVR".
If it says "Oculus is set as the Active OpenXR Runtime", then fear not, step 3 will solve this.
![](https://github.com/Kvitekvist/FUS/blob/main/images/oculus%20wrong%20openxr.jpg?raw=true)
This was verified on version Oculus App Version 59.0.0.138.366.

### Step 3 - Openxr in SteamVR
![](https://github.com/Kvitekvist/FUS/blob/main/images/steamvr%20openxr.jpg?raw=true)

Open Steam, then launch SteamVR.
Go to Settings in SteamVR and click on OpenXR.
If it says "Current OpenXR runtime: Oculus" then click on "Set steamVR as openxr runtime".
If it says "Current OpenXR runtime: SteamVR" then you are good.

![](https://github.com/Kvitekvist/FUS/blob/main/images/working%20oc.jpg?raw=true)

This was verifed on version 2.0.10 of SteamVR.

### Step 4 - Check opencomposite in the optional mod in FUS.
Find the opencomposite mod category at the top, and select "Skyrim VR OpenComposite Fixes Custom Build". This will make the game launch with opencomposite.

![](https://github.com/Kvitekvist/FUS/blob/main/images/opencomposite-selected.jpg?raw=true)

Next, there are some Controller Stabilizer options you also can add on. It will make hand motions smoother at the cost of some latency. We find that Low is a good place to start with. The high option feels quite nice for archery, but not as great with melee or magic attacks. 

### Step 5 - Launch FUS
At this step, verify that the little steamvr window says "Now Playing - OpenComposite_SkyrimVR". If it does, then you are now playing FUS with opencomposite.

## Method 2 - Set all openxr runtimes to VDXR
This method should in theory give better performance than using steamvr as openxr runtime.

### Step 1 - Close steamvr
SteamVR must not be running while using VDXR as runtime. 

### Step 2 - Openxr in Virtual Desktop Streamer on the desktop PC.
Open the Virtual Desktop Streamer and go to Options.

![](https://github.com/Kvitekvist/FUS/blob/main/images/VD%20streamer%20vdxr.jpg?raw=true)

In the OpenXR Runtime, choose "VDXR" from the dropdown list.
This was verified on version 1.29.8 of Virtual Desktop Streamer (non-steam version. I used the one from the website). No beta version required.

### Step 3 - Verify that "VDXR" is set as openxr runtime in steamvr on PC Desktop.
![](https://github.com/Kvitekvist/FUS/blob/main/images/steamvr%20vdxr.jpg?raw=true)

Open steamvr, and go to Settings.
Then click on the OpenXR tab. Here is should now say "Current OpenXR runtime: VirualDesktopXR (Bundled).
Once verified, close steamvr again.

### Step 4 - Launch FUS
At this step, verify that the little steamvr window says "Now Playing - OpenComposite_SkyrimVR". If it does, then you are now playing FUS with opencomposite with Virtual Desktop.

![](https://github.com/Kvitekvist/FUS/blob/main/images/working%20oc.jpg?raw=true)


# Launching issues
Step 1 - Double check step 1-3. Then try launching again.

Step 2 - In FUS, scroll to the bottom, there you find a mod named "Overwrite". Right click on it and choose "Clear Overwrite". Then try launching again.

Step 3 - Disable ReShade and Upscaler mod (DLSS, DLAA or FSR), then clear the overwrite again. Then try launching.

Step 4 - ENB and VR Performance Kit is not offically supported in FUS. If you are using these, then go back an clean your SkyrimVR as per the clean install instructions here: https://github.com/Kvitekvist/FUS/wiki/Prepare-PC-for-modlist#clean-skyrim