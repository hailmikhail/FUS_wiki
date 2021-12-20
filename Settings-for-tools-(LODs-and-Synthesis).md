[Back to Readme](https://github.com/Kvitekvist/FUS/blob/main/README.md)

* [Creating LODs for FUS](#creating-lods-for-fus)
   * [Deletion of current LOD files](#deletion-of-current-lod-files)
   * [xLODGen](#xlodgen)
   * [TexGen](#texgen)
   * [DynDOLOD](#dyndolod)
* [Synthesis Patcher](#synthesis-patcher)

# Creating LODs for FUS

A few things are impoartant when you want to create your own LODs. Create them in the right order, choose the right compression and before you start you should delete all the lod output files.

Now, lets go through the process.

## Deletion of current LOD files
To delete the currently created LOD files, you need to delete the content of 3 folders (inside FUS\mods). NB do not delete the folder itself, only what is inside. We are reusing these folders and the names matter for the load order).

NOTE: Most likely you do NOT want to delete `xLODGen_Output`. It is only necessary to do this if you change the landscape textures. We currently do not provide the tool to recreate them.

```
xLODGen_Output
TexGen_Output
DynDOLOD_Output (low - mid - high, depending on which option you used. You can delete all, just to be sure).
```

## xLODGen
The first lod files we create are the xlodgen files. This is terrain LODs. To create them, you will need to download xLODGen and set it up in MO2, we currently do not ship FUS with this tool.

We are using these settings:

![image](https://github.com/Kvitekvist/FUS/blob/main/images/lod%20settings/xlodgen_settings.png?raw=true)

Make sure you select all the worldspaces and make sure you update the values for all 4 lod settings.
We are only using Terrain LODs. 

After this has ran, copy the output and paste it into the xLODGen_Output. Press F5 to update MO2, and make sure that xLODGen_Output is an active mod. Then optionally you can run Cathedral Asset Optimizer to transform the mod to a .bsa archive which is faster to load when the game starts. This is not necessary, if you don't want to do it, just remove the previous .bsa and .esp files.

## TexGen
This will create LOD textures for us. Run `TexGen64` in MO2, then follow these settings:

![image](https://github.com/Kvitekvist/FUS/blob/main/images/lod%20settings/texgen_settings.png?raw=true)

Feel free to test different texture sizes. We are focusing on performance and find that these settings work fine.
What you should be aware of is that we are using BC3 compression. This is strongly recommended for VR.

When this has finished running, place the output into Texgen_output. Press F5 to update MO2, and make sure that Texgen_output is an active mod. Then optionally you can run Cathedral Asset Optimizer to transform the mod to a .bsa archive which is faster to load when the game starts. This is not necessary, if you don't want to do it, just remove the previous .bsa and .esp files.

## DynDOLOD

This will create the final LODs. Run `DynDOLODx64` in MO2, then select `Advanced >>>`, then you have three presets provided by us:

* Low: uses low standard DynDOLOD settings and billboard tree LODs
* Mid: uses medium standard DynDOLOD settings and performance 3D tree LODs -> default option
* High: uses high standard DynDOLOD settings and quality 3D tree LODs -> very performance-intensive, only recommended for high-end PCs

To get these presets, just press `Load preset` at the bottom left of the DynDOLOD Advanced window. You do not have to change anything else, these presets work fine for the FUS list. If you added things to the world and find them missing in the LODs after you ran DynDOLOD, you can recreate the presets for your current load order by newly loading the DynDOLOD rules of your choice and setting the rules for trees (bottom of the rule window) like we have it in our preset of your choice.

After this has ran, copy the output and paste it into the DynDOLOD_Output folder of your choice. Press F5 to update MO2, and make sure that DynDOLOD_Output is an active mod before going to the next step. Do not run Cathedral Asset Optimizer on the DynDOLOD files.

# Synthesis Patcher

Every time you create new LODs and every time you change anything in the weather setup then you should also rerun Synthesis with these patchers enabled:

1. SkyVRaanWeatherPatcher
2. SkyVRaanAutoPatcher
3. SynFloraFix
4. Khajiitearsshow
6. LootableCrates
7. SpellAbsorbFix

You only need to run it, it automatically overwrites the previous synthesis.esp file.