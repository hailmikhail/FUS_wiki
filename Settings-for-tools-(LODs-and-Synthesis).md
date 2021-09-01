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

xLODGen_Output
TexGen_Output
DynDOLOD_Output_quality / DynDOLOD_Output_performance (depending on which option you prefer. You can delete both, just to be sure).

## xLODGen
The first lod files we create are the xlodgen files. This is terrain LODs.
We are using these settings:

![image](https://github.com/Kvitekvist/FUS/blob/main/images/lod%20settings/xlodgen_settings.png?raw=true)

Make sure you select all the worldspaces and make sure you update the values for all 4 lod settings.
We are only using Terrain LODs. 

After this has ran, copy the output and paste it into the xLODGen_Output. Press F5 to update MO2, and make sure that xLODGen_Output is an active mod before going to the next step.

## TexGen
This is the most simple one to run. This will create LOD textures for us. Follow these settings:

![image](https://github.com/Kvitekvist/FUS/blob/main/images/lod%20settings/texgen_settings.png?raw=true)

Feel free to test different texture sizes. We are focusing on performance and find that these settings work fine.
What you should be aware of is that we are uxing BC3 compression. This is strongly recommended for VR.

When this has finished running, place the output into Texgen_output. Press F5 to update MO2, and make sure that Texgen_output is an active mod before going to the next step.

## DynDOLOD

Here you have two options, performance or quality.

### Performance version

These are the recommended performance settings:

![image](https://github.com/Kvitekvist/FUS/blob/main/images/lod%20settings/dyndolod_performance_settings.png?raw=true)

Make sure to select all the world spaces. Then click on Low (The difference between no LOD and low is massive, but the difference between low and medium is subtle).

Next, scroll all the way down to Trees and update the values as shown in the screenshot.
Make sure to follow all the other options from the screenshot as well. Then press Ok.

After this has ran, copy the output and paste it into the DynDOLOD_Output_performance. Press F5 to update MO2, and make sure that DynDOLOD_Output_performance is an active mod before going to the next step.

# Synthesis Patcher

Every time you create new LODs and every time you change anything in the weather setup then you should also rerun Synthesis with these patchers enabled:

1. SkyVRaanWeatherPatcher
2. SkyVRaanAutoPatcher
3. SynFloraFix
4. Khajiitearsshow
5. DisplaySpellTomeLevelPatcher
6. LootableCrates
7. SpellAbsorbFix