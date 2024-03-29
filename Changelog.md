[Back to Readme](https://github.com/Kvitekvist/FUS/blob/main/README.md)

The latest release can always be found on the [release page](https://github.com/Kvitekvist/FUS/releases)!

THE RELEASE PAGE NOW CONTAINS THE CHANGELOG DIRECTLY! Below you can find old changelogs for reference.

## Version 1.1.0
### General Notes

+ Toggle off then on Essential Files after the update.
+ Mods that don't work with open composite are marked with "[No OC]"
+ New ini files are available on the git repository with three different quality levels. Download and put into the profile folder that you use within the FUS install folder


### Mods added

+ Pull Mastery Hookshot or Grappling hook(SE)


### Mods updated

+ Spell Wheel
+ Blended Roads
+ Immersive Sounds - Compendium
+ Engine Fixes VR
+ Landscape Fixes For Grass Mods
+ Drop on Death
+ HIGGS
+ Cathedral - Armory


### Mods Removed


### Bug Fixes

+ Removed flying barrel over Whiterun giant camp


### Other

+ Moved 3 audio mods into essential part to prevent NPCs not having voice audio in FUS profile
+ Moved 3D audio into essential files
+ Updated ini files
+ Medium profile by default
+ disable tree animations in all inis for performance reasons

## Version 1.0.10

Submission to the official Wabbajack list server. Nothing relevant changed for users.

## Version 1.0.9

Minor update, but big performanc upgrade, most impact outside Whiterun. 
Save file compatible with version 1.0.8.1 test
Backup of loadorder is updated for each profile

### Mods added
+  Lightened Skyrim (1-2 better MS)
+ Skyrim Landscape and Water Fixes
+ Custom grass patch for Whiterun (We got as much as 20-30 more FPS outside whiterun during tests)

### Mod updates
+ Synthesis

### Ini updates
+  fsneakheightpercent = 0

## Pre-release Versions 1.0.6 to 1.0.8

These were test versions as we changed no mods but only tinkered with the in files and Bilago's tool and tested some performance stuff. 

## Version 1.0.5

This is a hotfix update. 

Some mods were not included in the 1.0.4 modlist because of a missing flag to include them. VrVision preset has been updated. If you were using VrVision previously, we recommend that you open the MO2 ENB tool, then toggle off then back on the VrVision option. Green Tundra Patch was removed as it was intended to be removed. New xLodgen files were generated. All light options for LUX are now available as well. Backup options to restore load order is also updated.

You need to press the ["restore" button](https://github.com/Kvitekvist/FUS/blob/main/images/restore%20loadorder.png) of your profile!

## Version 1.0.4

### Comments
Principally safe to update on an ongoing save, but you need to check if the correct mods are still enabled for you. We disabled some mods by default now to not make the game more difficult than vanilla by default. Just enable them again :) Skyrim will also tell you that mods are missing when loading a save.

We changed the profile names to be more accurate. Wabbajack does not delete profiles though. This is in case users make their own profiles.
So, all users who updated now have the old profiles plus the new ones. You can delete the old profiles or change profiles from the dropdown. This is not an issue for brand new users.

### Mods added
+ [Serveral LUX options](https://github.com/Kvitekvist/FUS/wiki/LUX-optional-mods)
+ True Storms and Azurite Patch
+ The Grass Your Mother Warned About
+ The Grass Your Mother Warned About (OPTIONAL Rift Fallen Leaves Options)
+ Waymark - A Road Signs Mod
+ Static Mesh Improvement Mod - SMIM (Light version)
+ Landscape Fixes For Grass Mods
+ Landscape Fixes For Grass Mods (Great cities patch)
+ Landscape Fixes For Grass Mods (The Grass Your Mother Warned About Patch)
+ Cathedral - 3D Pine Grass (Full 3D Coverage)
+ Cathedral - 3D Pine Grass (High Poly Green Grass Update)
+ Clean Menu - VR Edition
+ aMidianBorn Book of Silence SE -- CREATURES
+ Septentrional Landscapes SE - 2K
+ Hyperborean Snow SE - 2K
+ Northern Shores SE - 2K
+ Auto Sneak and Jump VR
+ VR Menu Mouse Fix

### Mods updated
+ HIGGS
+ Dual Wield Block VR
+ patch - azurite weathers
+ DynDOLOD Resources SE 3
+ xlodgen output
+ texgen output
+ dyndolod output
+ Syntheis

#### Synthesis patches
+ SkyVRaanWeatherPatcher
+ SkyVRaanAutoPatcher
+ Florafixer
+ Khajiitearsshow
+ DisplaySpellTomeLevel
+ LootableCreates
+ SpellAbsorbFix

### Mods removed
+ Cathedral Landscape
+ Point the way (Replaced by Waymark)

### Other
+ Packed xLodgen and texgen to BSA to improve MO2 boot time.
+ Added FUS welcome message in character creation
+ Added update option for skyrim.ini in the Essential Files manager
+ Changed name from "Visuals" to "Apperance" on the profiles
+ Changed mod position for Nobel.
+ Fixed Category numbers
+ Unchecked a few mods by default
+ Disabled all features from MageVR except the backpack.
+ Fixed a spellforge base library issue

### INI Updates
ini files need updating.
Download them from here:
https://github.com/Kvitekvist/FUS/tree/main/ini

skyrimvr.ini + skyrimprefs.ini goes into the 3 profiles folders:
profiles\FUS (Basic)
profiles\FUS RO (Basic + Appearance)
profiles\FUS RO DAH (Basic + Appearance + Gameplay)

skyrim.ini goes into the folder where skyrimvr.exe is located: steam\SkyrimVR

## Version 1.0.3

HOTFIX!

### Fixes
+ Replaced Strange runes for LE with the correct VR version

## Version 1.0.2

New save required!

### Mods added

+ Populated Forts Towers Places Remastered Edition
+ Populated Dungeons Caves Ruins Legendary
+ Bethesda logo remover (fixes the overlaying logo when in the starting game menu)

### Fixes

+ Unintended “Skyrim Revamped Loot and Encounter Zones” plugin from OMEGA AIO was removed (made the game way too difficult)

### Mods removed

+ OMEGA AIO


### Other

+ Changed player name to “Adventurer”
+ Moved SOSCBO to melee gameplay (yellow)
+ Updated dummy plugins
+ Make new backup of mod order
+ Make new backup of plugin order
+ Added version header into MO2

## Version 1.0.1

### Mods added

+ True Storms
+ DummyPlugins (one for each profile, meaning if mods are disabled these plugins will stay and preserve the loadorder)
+ Strange Runes as optional mod
+ Obsidian Mountain Fog
+ FUS_TrueStorm_Patch (also uploaded to Nexus)


### Fixes

+ Profiles are renamed to "FUS", "FUS RO", and "FUS RO DAH"
+ Basic and Basic + Visual profiles are now included. I messed up so WJ only included the main profile FUS RO DAH.
+ Fixed load order of several mods (Synthesis and a few others)
+ Mod Category 3 (orange ones) are all marked as optional mods. Add the ones you want, you do not need all. But see if you also need any of the patches.
+ Added a "restore" backup of mod order and load order, in case you mess it up. Now you can click on the restore button in MO2, to restore the list back to default sorting.
+ Iron starting gear is removed from character creation.

### Mods removed

- Spellforge - Vokrii patch (there was no patch for this)

### Important note about Load Order
You can activate or deactivate any mod marked as optional. Load order will be preserved. DO NOT RUN LOOT. If you add mods yourself, sort them manually. Best general tip is to have the plugins sorted in the same order as the mods. There are exceptions, so this is a general advice.

### Tools are missing?
We have decided not to include most of the tools we use when developing the modlist. This is not because we don't want to share how we do things. In fact we added all this in the readme above. We have excluded the tools because if a tool hosted on GIT is updated the list goes down which is a typical Dyndolod issue. LOOT is removed because running it will break the modlist. 

We are also continuously working on improving the readme!