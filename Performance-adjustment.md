[Back to Readme](https://github.com/Kvitekvist/FUS/blob/main/README.md)

# Performance adjustment

First of all, we recommend playing the game on a render resolution of 100% (SteamVR) or 1.0 (Oculus). If you have an increased render resolution, your performance will suffer. On Oculus quest, we actually recommend a lower render resolution of 0.7 (see below for [Quest settings](#a-note-on-oculus-quest)).

Then, FUS comes with a few options that can be changed in order to get the best performance for your system.

## How to check performance

Several tools exist for this. If you have an Oculus (Meta) device, you can open the [debug tool](https://developer.oculus.com/documentation/native/pc/dg-debug-tool), then on the HUDs section "Visible HUD" dropdown choose "Performance". Then you will get an FPS and headroom counter while u play. You can also use [fpsVR](https://store.steampowered.com/app/908520/fpsVR/), or you can just use the native SteamVR Advanced Frametimer if you are on SteamVR:

![Frametimer](https://github.com/Kvitekvist/FUS/blob/main/images/frametimer.png)

All tools give you some sort of understanding how much your GPU is doing while you play.

### What the numbers mean

You will see frame times for CPU and GPU there. This means the time it takes for your CPU (processor) or GPU (graphics card) to create the next image for your display. This needs to be **bewlow** 1/refresh rate, i.e. 1/90 Hz = 0.0111 seconds = 11.1 ms for the HTC Vive. Or you can choose to force reprojection always on and increase the refresh rate again, e.g. I am playing on a Valve Index set to 144 Hz but forced reprojection (leading to 72 Hz effective refresh rate), which in turn means my frametime must be below 1/72 = 0.0138 = 13.8 ms.

### For Quest users - Oculus Debug Tool
![image](https://github.com/Kvitekvist/FUS/blob/main/images/aws.jpg?raw=true)

#### Setting fixed (half frame rate) (1)

With ASW (Asynchronous SpaceWarp) you can do two things. You can cap the refresh rate, and you can cap the refresh rate plus adding reprojection.
If you struggle to keep max fps during your play, you might want to try this. For me (Kvitekvist), it feels much better to have a fixed FPS all the time, compared to having variable frame rates.
To do this, simple activate Asynchronous Spacewarp and set it to "Force 45 FPS, ASW Disabled". The number 45 is a little misleading. It actually means "Cap fps at half of your headsets refresh rate".
So, if you have a Quest1 with 72 mhz refresh rate, then your capped frame rate will be 36. If you have 90 mhz, then you will have 45 FPS, and if you have 120 mhz then you will get 60 FPS.
With the second option, "Force 45 FPS, ASW Enabled", you get the same effect as above, but you also get a sort of motion smoothing effect:

"Asynchronous SpaceWarp (ASW) is a frame-rate smoothing technique that almost halves the CPU/GPU time required to produce nearly the same output from the same content."
You can read more about it ![here](https://developer.oculus.com/documentation/native/pc/asynchronous-spacewarp/)"

Some people really like this, others do not (as it also introduces some sort of ghosting effects).


#### Checking Performance on Quest (2)

Using the Debug tool (see screenshot) then you can enable the Performance overlay HUD.
Then, when the headset is active, you can see your current App frame rate hz (3) and your current headroom (4)

Consider App Frame Rate your FPS number. If you see this dipping a lot, then your hardware / software settings are not able to keep up, and you might benifit from activating ASW.

The Performance Headroom is an indicator of how much load you are under. A high number is good, a low number is bad. Bad means you might experience stutter or skipped frames.

**Important!** 

If your GPU is not at max load, but you still see reprojection, this is perfectly normal. This means your PC is not able to create new images every time the display refreshes, so it reprojects the old one. This gives your GPU more headroom (= less usage), but you will see a chopper image. This can be caused by both the CPU and the GPU not being fast enough. It looks like a GPU load of 70% means you are fine, but you cannot rely on this. The only measure that is valid is the frametime! 

## How to adjust performance

In FUS there are five main options to improve performance:

* **Fixed Foveated Rendering (FFR):** In the [essential files activation step](https://github.com/Kvitekvist/FUS/wiki/Activate-the-Essential-Files) you can use fixed foveated rendering to improve your performance. This is not compatible with OpenComposite or FSR, and it does give a slight flicker in the very edges, but you can adjust the rings in the configuration of FFR to tweak it until you are happy with it. If you change the stuff best change it directly in the Skyrim VR base game folder and make a backup so in case it gets overwritten by a new FUS update you can use your settings again. The defaults we provide are giving a slight performance improvement while having almost no impact on the visuals.
* **The Reshade/ENB presets:** We provide several ENBs and more lightweight reshade options as explained [here](https://github.com/Kvitekvist/FUS/wiki/Choose-ENB-or-Reshade). The lightest we recommend is `The Sharper Eye` which has an almost negligible impact on performance. We also recommend `Glamur` which uses an extra sharpener and adds ambient occlusion and global illumination, but this comes at an additional performance cost. It isn't that much more costly but on low-end GPUs it might be too much. If you use an ENB these come with more additional costs.
* **The DynDOLOD presets:** We provide three presets for DynDOLOD which will have different impact on your visuals and on your performance. You can see them directly in MO2 at the bottom in the blue "Optional Late LOD Files". Only choose one! `DynDOLOD_Output - mid` is the default and uses medium DynDOLOD settings and 3D tree LODs (so called ultra trees - not to be mixed up with the actual 3D trees mod, which we do not use) with decent performance. `DynDOLOD_Output - low` is still looking fine, it uses the low DynDOLOD preset and regular flat tree billboards. If you really want to go crazy and have the performance headroom, you can use `DynDOLOD_Output - high`, which uses high DynDOLOD rules and a better quality 3D tree LOD model.
* **The ini files:** We provide three different ini quality presets. By default the "Medium" preset is selected, but you can try the low or high preset and / or play around with the values yourself. You will find all presets in your FUS folder in `FUS\tools\Ini options`. Here you can see three folders, go into the folder you want to use and copy the **content** of the folder into the profile folder that you are using, e.g. `FUS\profiles\FUS RO DAH (Basic + Appearance + Gameplay)`. You can try out different presets and open the files to see their values and adjust to your explicit needs.
* **Grass density:** Although we adjust grass density in our ini presets, grass is always one of the hardest hitter in Skyrim VR and you might have to further reduce it. We removed the ini from the mod itself and you can adjust the grass density using Bilago's INI configuration tool within MO2. In the dropdown menu of what to start (shows `Play FUS (SKSE)` by default) in MO2, select the `INI Configuration Tool`, then press `Run`. Inside the tool, filter for "imingrasssize", which should be 80 by default. You need to **increase** that value to **decrease** the grass density, it is an inverse relationship! E.g. set it to 90 or 100 if you need better performance. Conversely, you can decrease it to 70 or 60 if you have a beefy PC.

## A note on Oculus Quest and other Oculus (Meta) devices

A very easy way to improve performance on Oculus devices is to use "OpenComposite" in the essential files selection. This will break Virtual Desktop and Mage VR (so you cannot use either of these anymore), but the added performance is worth it. You can expect a 10-20% performance improvement. 

#### With open composite, you will see VIVE Wands instead of Quest controllers. 
This is just a visual feature (described on opencomposite github) and there is no fix, but quest controllers and buttons still work as intended.

By default, we have included an opencomposite.ini that gets placed into the folder where skyrimvr.exe is located. This is where you can adjust supersampling for Skyrim VR specifically. The default setting here is 1.0 (100%). You can increase or decrease this value to adjust supersampling, even values as low as 0.7 might make sense to save performance.

The Quest does not make best use of the pixels, so the best is to actually subsample by setting the render resolution to 0.7 as mentioned above. Oversampling will lead to compression artifacts and the Quest cannot actually make use of the pixels since it does not get the native image via link, but a compressed version. If you find the game too blurry try slowly increasing this value back to not more than 1.0 again.

Also, keep in mind that supersampling stacks. So make very sure that you only adjust supersampling in one tool.
If you use OpenComposite, then set the ss in the opencomposite.ini, have all other options set to 1.0
If you do not use OpenComposite, then set the ss in steamVR, have all other options set to 1.0.

### Stuff that doesn't work with OpenComposite
1. Virtual Desktop
3. MageVR

If you do not want to use OpenComposite, we recommend using Fixed Foveated Rendering instead (see above).