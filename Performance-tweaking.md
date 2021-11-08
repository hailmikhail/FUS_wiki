[Back to Readme](https://github.com/Kvitekvist/FUS/blob/main/README.md)

# Performance tweaking

First of all, we recommend playing the game on a render resolution of 100% (SteamVR) or 1.0 (Oculus). If you have an increased render resolution, your performance will suffer. On Oculus quest, we actually recommend a lower render resolution of 0.7.

Then, FUS comes with a few options that can be changed in order to get the best performance for your system.

## How to check performance

Several tools exist for this. If you have an Oculus (Meta...) device, you can open the debug tool, then on the HUD Display dropdown choose "Performance". Then you will get an FPS and headroom counter while u play. You can also use [fpsVR](https://store.steampowered.com/app/908520/fpsVR/), or you can just use the native SteamVR Advanced Frametimer if you are on SteamVR:

![Frametimer](https://github.com/Kvitekvist/FUS/blob/main/images/frametimer.png)

All tools give you some sort of understanding how much your GPU is doing while you play.

### What the numbers mean

You will see frame times for CPU and GPU there. This means the time it takes for your CPU (processor) or GPU (graphics card) to create the next image for your display. This needs to be **bewlow** 1/refresh rate, i.e. 1/90 Hz = 0.0111 seconds = 11.1 ms for the HTC Vive. Or you can choose to force reprojection always on and increase the refresh rate again, e.g. I am playing on a Valve Index set to 144 Hz but forced reprojection (leading to 72 Hz effective refresh rate), which in turn means my frametime must be below 1/72 = 0.0138 = 13.8 ms.

**Important!** 

If your GPU is not at max load, but you still see reprojection, this is perfectly normal. This means your PC is not able to create new images every time the display refreshes, so it reprojects the old one. This gives your GPU more headroom (= less usage), but you will see a chopper image. This can be caused by both the CPU and the GPU not being fast enough. It looks like a GPU load of 70% means you are fine, but you cannot rely on this. The only measure that is valid is the frametime! 

## How to adjust performance

In FUS there are four main options to improve performance:

* **The Reshade/ENB presets:** We provide several ENBs and more lightweight reshade options. The lightest we recommend is "VR Vision" which has a low impact on performance. However, it still uses an extra Luma sharpener, which can be taxing for older GPUs and may not be worth it then. So, if you have performance troubles, the the first thing you should do is to disable that sharpener. The easiest way to do it is the Reshade overlay, by pressing the `home` key when the game is running, then untick the extra sharpener. Keep the VR_CAS_Color effect enabled! Another option is to go into the reshade config file at `FUS\tools\ENB\Games\SkyrimVR\Presets\06 - Low - VRVision\Reshade\Presets` and open the "VRVision 3.ini" file with a text editor. Here, delete "prod80_05_LumaSharpen@PD80_05_Sharpening.fx," in line 3, save, start the game. Conversely, if you have performance headroom and want to improve your image quality, you can try a different ENB. Remember to disable your tonemapper in the ini configuration tool, as explained [here](https://github.com/Kvitekvist/FUS/wiki/Choose-ENB-or-Reshade).
* **The DynDOLOD presets:** We provide two presets for DynDOLOD which will have different impact on your visuals and on your performance. You can see them directly in MO2 at the bottom in the blue "Optional Late LOD Files". Only choose one! "DynDOLOD_Output_quality" is the default and uses 3D tree LODs (so called ultra trees - not to be mixed up with the actual 3D trees mod, which we do not use) and a high preset in DynDOLOD. "DynDOLOD_Output_performance" is still looking totally fine, it uses the medium DynDOLOD preset and regular flat tree billboards. It still looks good tho, so don't hesitate to use that if your performance requires it!
* **Grass density:** Grass is always one of the hardest hitter in Skyrim VR. We removed the ini from the mod itself and you can adjust the grass density using Bilago's INI Confoguration Tool within MO2. In the dropdown menu of what to start (shows `Play FUS (SKSE)` by default) in MO2, select the `INI Configuration Tool`, then press `Run`. Inside the tool, filter for "imingrasssize", which should be 80 by default. You need to **increase** that value to **decrease** the grass density, it is an inverse relationship! E.g. set it to 90 or 100 if you need better performance. Conversely, you can decrease it to 70 or 60 if you have a beefy PC.
* **The ini files:** We provide three different ini quality presets. By default the "Medium" preset is selected, but you can try the low or high preset and / or play around with the values yourself. You will find all presets in your FUS folder in `FUS\tools\Ini options`. Here you can see three folders, go into the folder you want to use and copy the **content** of the folder into the profile folder that you are using, e.g. `FUS\profiles\FUS RO DAH (Basic + Appearance + Gameplay)`. You can try out different presets and open the files to see their values and adjust to your explicit needs.

## A note on Oculus (Meta) Quest

A very easy way to improve performance on Oculus devices is to use "opencomposite" in the essential files selection. This will break Mage VR, but the added performance is worth it. You can expect a 10-20% performance improvement. Additionally, the Quest does not make best use of the pixels, so the best is to actually subsample by setting the render resolution in the graphics tool to 0.7. Oversampling will lead to compression artifacts and the Quest cannot actually make use of the pixels since it does not get the native image via link, but a compressed version.