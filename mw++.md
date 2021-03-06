# MORROWIND++

Version 1.0.2 (February 11th)

[<< Back to Main](https://github.com/Sigourn/morrowind-improved/blob/master/readme.md#morrowind)  
[<< Back to Setup](https://github.com/Sigourn/morrowind-improved/blob/master/setup.md#setup)

## INDEX

- [Changelog](https://github.com/Sigourn/morrowind-improved/blob/master/mw++.md#changelog)
- [Introduction](https://github.com/Sigourn/morrowind-improved/blob/master/mw++.md#introduction)
  - [Following the setup guide](https://github.com/Sigourn/morrowind-improved/blob/master/mw++.md#following-the-setup-guide)
  - [Modding tips](https://github.com/Sigourn/morrowind-improved/blob/master/mw++.md#modding-tips)
  - [The Overwrite folder](https://github.com/Sigourn/morrowind-improved/blob/master/mw++.md#the-overwrite-folder)
- [Core module](https://github.com/Sigourn/morrowind-improved/blob/master/mw++.md#core-module)
- [UI and Hotkeys module](https://github.com/Sigourn/morrowind-improved/blob/master/mw++.md#ui-and-hotkeys-module)
- [Visuals module](https://github.com/Sigourn/morrowind-improved/blob/master/mw++.md#visuals-module)
- [Audio module](https://github.com/Sigourn/morrowind-improved/blob/master/mw++.md#audio-module)
- [Gameplay module](https://github.com/Sigourn/morrowind-improved/blob/master/mw++.md#gameplay-module)
- [Finishing touches](https://github.com/Sigourn/morrowind-improved/blob/master/mw++.md#finishing-touches)
  - [Install order and load order](https://github.com/Sigourn/morrowind-improved/blob/master/mw++.md#install-order-and-load-order)
  - [Conflict resolution](https://github.com/Sigourn/morrowind-improved/blob/master/mw++.md#conflict-resolution)
  - [Synchronizing mod masters](https://github.com/Sigourn/morrowind-improved/blob/master/mw++.md#synchronizing-mod-masters)
  - [Running Distant Land](https://github.com/Sigourn/morrowind-improved/blob/master/mw++.md#running-distant-land)
  - [In-game configuration](https://github.com/Sigourn/morrowind-improved/blob/master/mw++.md#in-game-configuration)
  - [Mod keybindings](https://github.com/Sigourn/morrowind-improved/blob/master/mw++.md#mod-keybindings)

## CHANGELOG

<details>
  <summary>v1.0.2 (February 11th)</summary>
  
- Added Facelift Textures (Core).
- Added Pluginless Khajiit Head Pack (Core).
- Added Mist Retexture (Visuals).
- Added Apel's Rain Replacer (Visuals).
</details>

<details>
  <summary>v1.0.1.1 (January 10th)</summary>
  
- Added instructions to hide a mesh from Morrowind Optimization Patch.
</details>

<details>
  <summary>v1.0.1 (January 4th)</summary>
  
- Minor formatting tweaks for readability.
- Minor update to MO2 messages' instructions.
- Removed Logo Intro Video Reworked, as **Setup** recommends the option to *Skip opening movie*.
</details>

<details>
  <summary>v1.0 (January 4th)</summary>

- Simplifcation of installation instructions.
- Deleted **Continuity** module, and redistributed mods accordingly.
- The following mods have changed categories:
  - Services Restored moved from Continuity to Core (Non-purist fixes9.
  - The Publicans moved from Continuity to Core (Non-purist fixes).
  - Improved Thrown Weapon Projectiles moved from Continuity to Visuals (Equipment).
  - Great Service moved from Core to Audio.
  - Sheep-no-More moved from Continuity to Audio.
</details>

## INTRODUCTION

### Following the Setup guide

The guide presented here assumes you have already followed the installation instructions found in the [**Setup**](https://github.com/Sigourn/morrowind-improved/blob/master/setup.md#setup) page. Please abstain from using this guide until you've correctly set up Morrowind.

### Modding tips

A crash course to Morrowind and Bethesda modding in general is:

- Don't uninstall mods mid-playthrough, and if you do, keep a pre-uninstallation savefile as a backup in case things go wrong.
- Read the description of every mod you install. Descriptions usually list requirements, compatibility issues, and known issues in a mod. This not only prevents future issues (or assures you they are "normal" or "expected"), but it also helps you decide beforehand whether a mod is worth the trouble.
- File structure matters when installing a mod. The file structure is how files are organized for the game to read these files and use them. Incorrect file structure accounts for a good deal of mods that don’t work properly. For instance, .esm and .esp files always need to be inside **Morrowind\Data Files**, or else the game simply won't register them. When a mod listed here has packaging issues, I will tell you how to fix them. Bear in mind that some mods do keep optional plugins in a separate folder, but these are the exception and descriptions usually make mentions of them.
- Some mods come with BSA files. These contain data files for the mod. The most popular mod which includes BSA files is the Tamriel Rebuilt project, which is not part of this guide. BSA files need to be registered in your Morrowind.ini file for the game to properly load the assets; failing to do so results in a well known problem of [**yellow exclamation triangles**](https://external-preview.redd.it/dl-I4l_Pzm5autet-87p1hnU1btUavtiu1mtwGzWBko.png?width=960&crop=smart&auto=webp&s=3d180a6476cad80c332c12be08252511a0044c5c). This particular guide, however, features no mods with BSA files. Broadly speaking, mods with BSA files tend to add lots of new assets into the game (meshes and textures), and this guide was designed with vanilla graphcis in mind.

When installing mods manually, by extracting the contents of a mod and dropping them inside your Data Files folder, there is a chance you will be overwriting one mod's files with another mod's. This is where mod managers come in: they make modding easy by providing you with lots of tools to aid you in modding your game.

**Mod Organizer 2** lets you hide specific files from your installed mods, including anything from meshes to textures, but also plugins. This is a especially useful feature when you deactivate certain plugins from a mod but don't want to see them cluttering up your load order, or you want certain files not to overwrite another mod's.

- To hide a plugin, right click on your installed mod and click **Information...**.
- Click the **Filetree** tab.
- Right click on the plugins, folders, or files you want to hide, and click **Hide**.
- Mod Organizer 2 will hide the files, and these will no longer affect your game.

### The Overwrite folder

One more quirk about Mod Organizer 2 is the **Overwrite** folder and how it ties together with the tools we installed in the **Setup** section. The **Overwrite** folder is the destiny folder for the output of many of these tools. For instance, Distant Land generation will place its contents here, inside the **distantland** folder. Files in the **Overwrite** folder will overwrite all your installed assets and plugins, should they have the same names and paths.

## CORE MODULE

### Bug fixes and optimization

- [**Patch for Purists**](https://www.nexusmods.com/morrowind/mods/45096) by half11  
The best unofficial fan patch for Morrowind.
- [**Correct UV Rocks**](http://mw.modhistory.com/download-56-12003) by Nich  
Fixes UV mapping on rocks and stones.  
- [**Morrowind Optimization Patch**](https://www.nexusmods.com/morrowind/mods/45384?) by Remiros and Greatness7  
Greatly improves performance and fixes some mesh errors.
  - In the BAIN installer, tick the following options only:
    - **00 Core**
    - **01 Fixed Vanilla Textures**
    - **02 Lake Fjalding Anti-Suck**
    - **03 MGE XE Addon**: if you plan to install tree replacers (like Vurt's) in the future, you should not install this option.
    - **05 Chuzei Fix**
  - Hide **meshes\f\furn_web10.nif**. This mesh causes a certain cobweb to lose transparency at a distance when using Intelligent Textures (present in this guide).
- [**Project Atlas**](https://www.nexusmods.com/morrowind/mods/45399) by the Project Atlas Team  
Optimizes the most performance heavy areas of vanilla Morrowind through texture atlases. 
  - In the BAIN installer, tick **00 Core** only.
  - Hide **meshes\x\ex_imp_plat_01.nif**. This mesh is buggy and can cause problems when traveling from Raven Rock to Fort Frostmoth using the boat.
- [**Creature VFX Restoration**](https://www.nexusmods.com/morrowind/mods/46194?) by rot  
Restores visual effects on creatures.
- [**Fix Those Bastard Rope Fences**](https://www.nexusmods.com/morrowind/mods/45741) by EJ-12 and Petethegoat  
Modifies collision boxes on rope-related meshes, player and NPC's hitboxes to prevent getting stuck.
- [**Glowing Flames**](https://www.nexusmods.com/morrowind/mods/46124) by PoodleSandwich  
Flames are now glow mapped and/or properly illuminated.
  - Install **Glowing Flames** only.
  - Hide *Glowing Flames - TrueLightsAndDarkness Tweaks.ESP*
- [**Expeditious Exit**](https://www.nexusmods.com/morrowind/mods/45634) by NullCascade  
Forces the game to instantly close on exit.
- [**Quest Skill Reward Fix**](https://www.nexusmods.com/morrowind/mods/48269) by Merzasphor  
Makes the game treat skill increases from quests as if there were raised via normal means, solving numerous problems with how the game treats these skill increases.
- [**Skill Increase GMST Fix**](https://www.nexusmods.com/morrowind/mods/48029) by Merzasphor  
Fixes several engine bugs related to GMSTs used when raising skills via NPC training and skill books.

### Non-purist fixes

- [**Services Restored**](https://www.nexusmods.com/morrowind/mods/47068?) by half11  
Adds the missing master trainer for Medium Armor, Cinia Urtius.
  - In [**TESAME**](https://github.com/Sigourn/morrowind-improved/blob/master/mwtools.md#tesame), delete the following records: 
    - NPC **hecerinde**
  - This omits the restoration of Hecerinde's Secret Master tools.
- [**The Publicans**](https://www.nexusmods.com/morrowind/mods/45410?) by half11  
Fixes several places in the vanilla game that are set up like inns, but in which Bethesda for some reason forgot to add the option to rent a room in.

### Expansion implementation

- [**Expansion Delay**](https://www.nexusmods.com/morrowind/mods/47588?) by half11  
Modifies how the Tribunal and Bloodmoon expansions are implemented into the game. This is an essential mod for anyone who thinks Bethesda's expansions deserved a better implementation.
- [**Early Transport to Mournhold**](https://www.nexusmods.com/morrowind/mods/47985) by Necrolesian  
Allows travel to Mournhold before the Dark Brotherhood attacks begin.

### HD textures

- [**Intelligent Textures**](https://www.nexusmods.com/morrowind/mods/47469) by Remiros  
Replaces almost all textures in the vanilla game and its expansions with high resolution AI upscales.
  - In the BAIN installer, tick **00 Core** and **01 Atlas Textures**.
- [**Facelift**](https://www.nexusmods.com/morrowind/mods/47617) by kartoffels  
Addresses numerous mesh issues with the vanilla head meshes, leading to much better looking faces overall.
  - Install **kart_facelift_meshes** and **kart_facelift_textures** only.
- [**Pluginless Khajiit Head Pack**](https://www.nexusmods.com/morrowind/mods/43110) by ashiraniir  
Pluginless replacer version of the 8 base khajiit heads.
  - Install **Pluginless Khajiit Head Pack - Whiskers Version** only.

## UI AND HOTKEYS MODULE

### HD UI

- [**Better Daedric Font**](https://www.nexusmods.com/morrowind/mods/44540?) by hardek  
High resolution replacer for the Daedric font used in scrolls. 
  - MO2 will tell you the content of data files does not look valid.
    - Right click on *data files*, and click *Create directory...*. Type **fonts** and click *OK*. 
  - Drag and drop **daedric_font.fnt** and **daedric_font_obw.tex** into **fonts**. Click *OK*.
- [**Better Dialogue Font**](https://www.nexusmods.com/morrowind/mods/36873) by Hrnchamd  
High resolution replacer for the Magic Cards font, used in most of the user interface.
  - Install **Better Dialogue Font** only.
- [**Comrade Raven's Book Arts Replacer**](https://www.nexusmods.com/morrowind/mods/48896?) by Alfred Khamidullin and Comrade Raven  
Replaces most of original book arts with hi-res images redrawn from scratch by Alfred “Hieronymus7Z” Khamidullin.
  - MO2 will tell you the content of data files does not look valid.
    - Right click the **Data Files** folder and click *Set as data files directory*. Click *OK*.
- [**Pete's Scroll 2018 ...in 2020**](https://www.nexusmods.com/morrowind/mods/47863/?) by Petethegoat  
Replacement scroll and journal textures, rendered out in 1k, 2k, and 4k dimensions.
  - Install **Pete's Journal and Scroll** only.
    - In the BAIN installer, tick **01 Journal and Scroll - 2K** only.
- [**Title Screen and Logo Video Intro Reworked**](https://www.nexusmods.com/morrowind/mods/43657) by Phobos  
HD recreation of the Title and Logo Intro, in widescreen.
  - Install **Title Screen Reworked (Widescreen)** only (assuming you enabled *Skip opening movie* in MGE XE).
- [**Widescreen Splash Replacer**](https://www.nexusmods.com/morrowind/mods/47163) by NZdawghaus  
Replaces the default splash screens with better quality widescreen versions (16:9), and adds three missing Bethesda splash screens.

### UI

- [**Better Questlist**](https://www.nexusmods.com/morrowind/mods/48272) by Virnetch  
Allows highlighting and hiding quests in the Journal questlist. Shift-Click on a quest to highlight it, Shift-Click again to hide and Shift-Click a third time to return to normal.
- [**Continue**](https://www.nexusmods.com/morrowind/mods/45952?) by Petethegoat  
Adds a continue button to the main menu to instantly load your most recent save.
- [**HUD Weapon Charge**](https://www.nexusmods.com/morrowind/mods/47962) by Virnetch  
Adds a fillbar that shows the currently equipped weapon's charge under the weapon condition bar on the HUD.
- [**New Game Confirmation**](https://www.nexusmods.com/morrowind/mods/47693?) by hardek  
Adds a confirmation popup when you click on New Game in the main menu.
- [**Shrine Tooltips**](https://www.nexusmods.com/morrowind/mods/48275) by Virnetch  
Adds tooltips with the effect's name to shrines when hovering over the different options.
- [**Smart Ammo**](https://www.nexusmods.com/morrowind/mods/47383?)  
Ammo autoequip while bow/crossbow/thrown weapon readied. It will remember and prefer last hand-picked ammo if pressing Alt while equipping it.
  - Also install [**MWSEabotlib**](https://www.nexusmods.com/morrowind/mods/47717).
- [**Smart Journal**](https://www.nexusmods.com/morrowind/mods/47492?) by abot  
Adds several new options for the journal and quest pages.
- [**Smart Map**](https://www.nexusmods.com/morrowind/mods/46634)  
Automatically switches between the local and world map depending on user configuration.
  - Also install [**MWSEabotlib**](https://www.nexusmods.com/morrowind/mods/47717).
- [**UI Expansion**](https://www.nexusmods.com/morrowind/mods/46071?) by NullCascade  
Expands UI functionality with searching, filtering, and more visual feedback.

### Hotkeys

- [**Book Pickup**](https://www.nexusmods.com/morrowind/mods/46625) by NullCascade  
Enables picking up books by default, instead of opening them. This can be disabled by holding shift. The behavior can be inverted using the mod config menu.
- [**Hotkeys Extended**](https://www.nexusmods.com/morrowind/mods/48055) by Virnetch  
Expands the vanilla Quick Menu by adding different hotkeys for holding or double tapping a button and/or when holding a specific button. All hotkeys use the same keys as in vanilla. In total there can now be 81 different hotkeyed items/spells.
- [**Quick Equip**](https://www.nexusmods.com/morrowind/mods/48341) by Merlord  
Holding down a hotkey (default left shift) while clicking an item in your inventory will equip that item instead of picking it up. 
- [**Right Click Menu Exit**](https://www.nexusmods.com/morrowind/mods/48458) by Merlord  
Exit any menu by right clicking (or whatever your menu key is mapped to).
- [**Security Enhanced**](https://www.nexusmods.com/morrowind/mods/47038) by OperatorJack  
Adds hotkeys for lockpicks and probes, as well as hotkey cycling options, ordering options, and auto-equip options for activating locked or trapped objects.
- [**Torch Hotkey**](https://www.nexusmods.com/morrowind/mods/45747?) by Remiros, Greatness7, and NullCascade  
Adds "C" as a dedicated hotkey for light sources. It will equip/unequip the first light source in your inventory when pressed and prioritizes already used lights. It will also re-equip previously equipped shields, two-handed weapons and ranged weapons.

## VISUALS MODULE

### Environment

- [**Better Waterfalls**](https://www.nexusmods.com/morrowind/mods/45424?) by Melchior Dahrk  
New effects and textures for the waterfalls. Includes LOD on the particle effects to improve performance.
- [**Waterfalls Tweaks**](https://www.nexusmods.com/morrowind/mods/46271) by multiple  
Reduces the water splash from **Better Waterfalls** to a more reasonable size.
- [**Bitter Coast Scum Replacer**](https://www.nexusmods.com/morrowind/mods/48291) by Anumaril21  
Replaces the scum found throughout the Bitter Coast using the animation method and edited textures of Tamriel Rebuilt's water statics and Pherim's Vanilla-Friendly Scum Texture.
  - In the BAIN installer, tick **00 Core** and **02 Animated Replacer - Greener Color** only.
- [**Near Vanilla Road Sign Replacer**](https://www.nexusmods.com/morrowind/mods/44957?) by Atrayonis
Makes road signs legible. Uses low resolution vanilla-friendly textures.
  - In the BAIN installer, tick **00 Core** and **01 Vvardenfell only** only.
- [**Remiros' Groundcover**](https://www.nexusmods.com/morrowind/mods/46733) by Remiros, vtastek, and Hrnchamd  
Adds groundcover to almost all regions.
  - Install **Remiros' Groundcover** only.
    - In the BAIN installer, tick **00 Core** and **04b Thicker Grass** only.
  - Also install [**Remiros' Groundcover Shaders - Landbias Fix**](https://cdn.discordapp.com/attachments/381217735306248192/769808563296010300/Remiros_Groundcover_Shaders__Landbias_Fix.7z), which will solve a very ugly problem with grass pop up if you have installed the shaders on the **Setup** page.
- [**Vivec Palace Water Replacer**](https://www.nexusmods.com/morrowind/mods/48291) by Anumaril21  
Replaces the water in the Palace of Vivec's canals.
  - In the BAIN installer, tick **00 Core** and **01 Original Color** only.

### Equipment

- [**Improved Thrown Weapon Projectiles**](https://www.nexusmods.com/morrowind/mods/44763?) by R-Zero  
Makes thrown weapon projectiles fly pointy end forward and, some of them, spin in the air.
  - MO2 will tell you the content of data files does not look valid.
    - Right click the **Data Files** folder and click *Set as data files directory*. Click *OK*.
- [**Weapon Sheathing**](https://www.nexusmods.com/morrowind/mods/46069) by TES3 Community
Equipped weapons will be shown on the character's hip or back. This new functionality affects both the player and all other characters, and works with all weapons from all mods. Additionally features a comprehensive set of high quality quiver and scabbard assets.
  - Install **WeaponSheathing 1.6-MWSE** only.
    - MO2 will tell you the content of data files does not look valid.
    - Right click the **Data Files** folder and click *Set as data files directory*. Click *OK*.
  - Also install [**Weapon Sheathing - Bow Position Edit**](https://www.nexusmods.com/morrowind/mods/48473?) by Kyim. The bows will better line up with the sheathing animation.
  - Also install the [**Morrowind Optimization Patch**](https://www.nexusmods.com/morrowind/mods/45384?) Weapon Sheathing Patch.
    - In the BAIN installer, tick **04 Weapon Sheathing Patch** only. Rename the mod to **Morrowind Optimization Patch - Weapon Sheathing Patch**.

### NPCS

- [**Yet Another Guard Diversity**](https://www.nexusmods.com/morrowind/mods/45894) by Half11, SkoomaPro, and Danke  
Replaces the generic, copy-pasted guards of Morrowind with different variations. Some guards have different loadouts and armor, and each have different faces.

### VFX

- [**Glow in the Dahrk**](https://www.nexusmods.com/morrowind/mods/45886) by Melchior Dahrk and NullCascade  
Makes windows glow in the dark.
  - In the FOMOD installer, install the following options:
    - Interior Sunrays.
    - Nord Glass Windows.
    - Raven Rock Glass Windows.
    - Hi-Res Window Texture Replacer.
  - Also install the [**Project Atlas**](https://www.nexusmods.com/morrowind/mods/45399) Glow in the Dahrk Patch.
    - In the BAIN installer, tick **10 Glow in the Dahrk Patch - Interior Sunrays** only. Rename the mod to **Project Atlas - Glow in the Dahrk Patch**.
- [**Mist Retexture**](https://www.nexusmods.com/morrowind/mods/44322) by Remiros  
Improves the texture for the mist. The mist is now much smoother and more detailed, as well as less opaque and flat. This also makes it play much nicer with SSAO.
  - Install **Mist Retexture** only.
- [**Subtle Magic Glow**](https://www.nexusmods.com/morrowind/mods/4468?) by atteSmythe  
Replaces the "plastic wrap" effect around in-game magic items (those equipped by characters or on the ground) with less-obtrusive versions.
  - In the BAIN installer, tick **faint** only.
- [**Subtle Smoke**](https://www.nexusmods.com/morrowind/mods/47341) by wazabear  
Makes it so many smoke effects are much more laid back and easier on the eyes.

### Weather and Lighting

- [**Apel's Rain Replacer**](https://www.nexusmods.com/morrowind/mods/42555) by Apel and HedgeHog-12  
Replaces rain with a more heavy rain look.
- [**Let There Be Darkness - Lua Lighting Overhaul**](https://www.nexusmods.com/morrowind/mods/47912/) by Greatness7, Merlord, OperatorJack, Petethegoat, and RedFurryDemon  
Configurable mod for automatical adjustment of lighting, including override values, cell whitelist, and light object editing.
  - Also install [**Let There Be Darkness v1.1 (No Level Design Lighting Preview Patch)**](https://www.mediafire.com/file/5vidcblah6g4tcy/Let+There+Be+Darkness+(No+Level+Design+Lighting+Preview+Patch).zip/file). Solves a compatibility issue with mods that use the **L** as a hotkey, such as Security Enhanced (present in this guide). Make sure you only install this mod for version 1.1 of Let There Be Darkness: it will likely not be compatible with older or newer versions.
- [**Weather Adjuster**](https://www.nexusmods.com/morrowind/mods/46816) by Hrnchamd  
Regional weather colours, skies and lighting. Visual weather editor and region-based presets. Seamless transitions between regions.
  - This mod lets you adjust many variables about Morrowind's weather. Read the description to learn how to do this. The reason I recommend it (aside because of how great the mod is) is that users can share their presets: the mod on its own will not change the appearance of the game until you configure it so.
- [**Weather Adjuster - Morrowind++ Preset**](https://www.mediafire.com/file/q99l3y9zezhdgjo/Weather+Adjuster+-+Morrowind+++Preset+v2.0.zip/file) by Sigourn  
Personal preset for darker nights and less horrible fog.
  - This mod has to be installed manually. Unpack the file and merge the **overwrite** folder with your Mod Organizer 2 **overwrite** folder, found inside the **Mod Organizer 2** folder. The contents of the folder should like so: **Mod Organizer 2\overwrite\MWSE\config\Weather Adjuster.json**.
  - [**Comparison here.**](https://imgsli.com/MTUwMjI)

## AUDIO MODULE

- [**Great Service**](https://www.nexusmods.com/morrowind/mods/47767) by Von Djangos  
Enables over 100 lines of voiced dialogue for shopkeepers that were shipped with the original game but never used.
- [**GreetDistanceReducer**](https://www.nexusmods.com/morrowind/mods/43994) by helswake  
NPCs will not shout at you as often when you walk by. They will still greet you, though, you just have to be a bit closer.
- [**No Female Nord Screeching**](https://www.mediafire.com/file/luyidl5yufsvfco/No+Female+Nord+Screeching+v1.0.zip/file) by Sigourn  
Replaces a handful of sound files to stop female Nords from bursting your ear drums when they are attacked.
- [**Sheep-no-More**](https://www.nexusmods.com/morrowind/mods/45168) by McChuggernaut  
Removes the sheep sounds from Morrowind.
- [**Shut the Fuck up Cliff Racers**](https://www.nexusmods.com/morrowind/mods/46588) by Merlord  
Drastically reduces the frequency of idle Cliff Racer screeches, by editing the kf file of the cliff racer mesh.

## GAMEPLAY MODULE

### Quality of life improvements

- [**Diligent Defenders**](https://www.nexusmods.com/morrowind/mods/45717?) by NullCascade  
When the player or the player's companions are attacked, any companions will launch into action in defense.
- [**Easy Escort**](https://www.nexusmods.com/morrowind/mods/45712?) by NullCascade  
Ensures that your followers get warped to you if they get too far away. Compatible with any follower from any mod, without any special script attached to that NPC.
- [**Graphic Herbalism - MWSE Edition**](https://www.nexusmods.com/morrowind/mods/46599) by Stuporstar and Greatness7  
Automatically harvests herbs, instead of opening the container interface. Picked herbs will now have their meshes modified or disappear altogether (they will still respawn).
  - In the BAIN installer, tick **00 Core + Vanilla Meshes** only.
  - Also install **GH Patches and Replacers**.
    - In the BAIN installer, tick **10 Atlas - Vanilla BC Mushrooms** only.
  - Also install [**Graphic Herbalism Lighting**](https://www.nexusmods.com/morrowind/mods/47864) by GrunTella. Picking a glowing plant will also remove the glow-light.
- [**MWSE Hide the Skooma**](https://www.nexusmods.com/morrowind/mods/48454) by Necrolesian  
Automatically hides your drugs so you don't have to dump them on the floor in order to trade.
- [**Pluginless and Adjustable Lower First Person Sneak**](https://www.nexusmods.com/morrowind/mods/48642) by Celediel  
Lowers the position of the first person camera when sneaking/crouching, making it easier to tell if you are sneaking. Adjustable on the fly.

### Leveling tweaks

- [**Improved Vanilla Leveling**](https://www.nexusmods.com/morrowind/mods/48065?) by Merzasphor  
Preserves vanilla leveling mechanics while eliminating the need to micromanage skill and attribute increases required to achieve optimal character progression.

### Balance

- [**Beware the Sixth House (Sixth House Overhaul)**](https://www.nexusmods.com/morrowind/mods/46036) by mort  
Makes the Sixth House, properly, the most difficult content in the game. Intended for use with Tribunal Rebalance and Bloodmoon Rebalance.
  - Note that unlike the Tribunal and Bloodmoon rebalances, this mod makes the game *harder*.
- [**Tribunal Rebalance**](https://www.nexusmods.com/morrowind/mods/45713) by mort  
Rebalances Tribunal as if it shipped with Morrowind. Intended to be used with Beware the Sixth House.
- [**Bloodmoon Rebalance**](https://www.nexusmods.com/morrowind/mods/45714) by mort  
Rebalances Bloodmoon as if it shipped with Morrowind. Intended to be used with Beware the Sixth House.

## FINISHING TOUCHES

### Install order and load order

The installation order dictates the priority a given mod's assets have over the mods' plugins installed before them. Respect this order to ensure assets are overwritten as intended.

<details>
  <summary>Install order</summary>

- DLC: Tribunal
- DLC: Bloodmoon
- MGE XE Data Files
- MGE XE Shader - 16 Lights Shaders Alpha
- MGE XE Shader - Deband Fogaware v2
- MGE XE Shader - EdgeAA
- MGE XE Shader - Specialprocess
- Patch for Purists
- Correct UV Rocks
- Morrowind Optimization Patch
- Project Atlas
- Creature VFX Restoration
- Fix Those Bastard Rope Fences
- Glowing Flames
- Expeditious Exit
- Quest Skill Reward Fix
- Skill Increase GMST Fix
- Services Restored
- The Publicans
- Expansion Delay
- Early Transport to Mournhold
- Intelligent Textures
- Facelift (Textures)
- Facelift (Meshes)
- Pluginless Khajiit Head Pack
- Better Daedric Font
- Better Dialogue Font
- Comrade Raven's Book Arts Replacer
- Pete's Scroll 2018 ...in 2020
- Title Screen Reworked (Widescreen)
- Widescreen Splash Replacer
- Better Questlist
- Continue
- HUD Weapon Charge
- New Game Confirmation
- Shrine Tooltips
- Smart Ammo
- Smart Journal
- Smart Map
- MWSEabotlib
- UI Expansion
- Book Pickup
- Hotkeys Extended
- Quick Equip
- Right Click Menu Exit
- Security Enhanced
- Torch Hotkey
- Better Waterfalls
- Waterfalls Tweaks
- Bitter Coast Scum Replacer
- Near Vanilla Road Sign Replacer
- Remiros' Groundcover
- Remiros' Groundcover Shaders - Landbias Fix
- Vivec Palace Water Replacer
- Improved Thrown Weapon Projectiles
- Weapon Sheathing
- Weapon Sheathing - Bow Position Edit
- Morrowind Optimization Patch - Weapon Sheathing Patch
- Yet Another Guard Diversity - Regular
- Glow in the Dahrk
- Project Atlas - Glow in the Dahrk Patch
- Mist Retexture
- Subtle Magic Glow
- Subtle Smoke
- Apel's Rain Replacer
- Let There Be Darkness - Lua Lighting Overhaul
- Let There Be Darkness (No Level Design Lighting Preview Patch)
- Weather Adjuster
- Great Service
- Greet Distance Reducer
- No Female Nord Screeching
- Sheep-no-More
- Shut the Fuck up Cliff Racers
- Diligent Defenders
- Easy Escort
- Graphic Herbalism MWSE
- GH Patches and Replacers
- Graphic Herbalism Lighting
- MWSE Hide the Skooma
- Pluginless and Adjustable Lower First Person Sneak
- Improved Vanilla Leveling
- Beware the Sixth House
- Tribunal Rebalance
- Bloodmoon Rebalance  
</details>

The load order dictates the priority a given mod's plugins have over the mods' plugins loaded before them. Respect this order to ensure plugin records are overriden as intended.

<details>
  <summary>Load order</summary>

- Morrowind.esm
- Tribunal.esm
- Bloodmoon.esm
- Patch for Purists.esm
- Patch for Purists - Book Typos.ESP
- Patch for Purists - Semi-Purist Fixes.ESP
- Lake Fjalding Anti-Suck.ESP
- chuzei_helm_no_neck.ESP
- Glowing Flames - NoMoreLightlessFlames v1.1.ESP
- Services Restored.ESP
- The Publicans.ESP
- Expansion Delay.ESP
- Early Transport to Mournhold.ESP
- Better_Typography_Bookarts_Fix.ESP
- Waterfalls Tweaks.ESP
- NearVanillaRoadSigns.ESP
- Yet Another Guard Diversity - Regular.ESP
- GITD_WL_RR_Interiors.ESP
- Great Service.ESP
- hw_GreetDistanceReducer.ESP
- Beware the Sixth House.ESP
- tribunal rebalance.ESP
- Bloodmoon Rebalance.ESP
- Merged Objects.ESP
- **Rem_AC.ESP**
- **Rem_AI.ESP**
- **Rem_AL.ESP**
- **Rem_BC.ESP**
- **Rem_GL.ESP**
- **Rem_Solstheim.ESP**
- **Rem_WG.ESP**

There are a couple of notes here:

- We will generated Merged Objects.ESP in a moment. For this process, make sure you deactivate all bolded plugins.
- The plugins from **Remiros' Groundcover** should only be enabled when generating Distant Land in MGE XE, and disabled when playing the game.
</details>

### CONFLICT RESOLUTION

TES3Merge lets us merge the objects in our active plugins in order to reduce conflicts, generating a **Merged Objects.esp** file which we will have to place at the end of our load order. This is very useful when, for example, you have a mod that modifies the stats on the Glass Armor while another modifies how it looks like: TES3Merge will merge both changes into a single plugin.

- Run TES3Merge in MO2. Once it's finished, press any key to exit.
- **Merged Objects.ESP** will now be present at the end of your load order.

### SYNCHRONIZING MOD MASTERS

Wrye Mash lets us synchronize the masters of mods we have installed. This will prevent certain error messages from popping up when launching the game.

- Run WryeMash in MO2.
- In the **Mods** tab, you will see a list with all your plugins, both active and inactive. Plugins that do not need to have their masters synchronized have a green box next to them. Those that do need to have their masters synchronized will have a box of a different color.
- Click on the faulty plugin, and a panel to the right will display the plugin's masters. Right click on either of them, and an *Update Masters* window will appear. Click *Yes*. 
- Once the window has closed, click on the *Save* button further below the same panel.

### RUNNING DISTANT LAND

MGE XE's Distant Land setup should be re-run. If you followed the steps [**in this section**](https://github.com/Sigourn/morrowind-improved/blob/master/setup.md#distant-land-tab) earlier, the process will be much easier.

- Run MGE XE in MO2.
- In the **Distant Land** tab, click *Distant land generator wizard*.
- Click *Select all*, and then *Continue*.
- Click *Run above steps using saved / default settings*.
- Once the statics have been created, simply click *Finish*.

### IN-GAME CONFIGURATION

**General adjustments**

Launch Morrowind and make the following adjustments.

- Under the **Options** menu, go to the *Video* tab.
- The *Gamma Correction* slider lets you increase/decrease the brightness of your game. I like to play Morrowind with the slider roughly 40-45% of the way from left to right, making the game look less washed out.
- Turn the *Real-time Shadows* slider all the way to the left, disabling them. These shadows look pretty bad, are glitchy, and not worth the performance hit.

The following mods require additional configuration through the in-game **Mod Configuration** menu.

**abot's Smart Journal**
- Set *Add a prefix in order to group quest names?* to *0*. This will remove the lag when opening the quest page without this option set to 0.
- (Optional) Disable every option below *Sort quests list by quest name?*. These options are mostly useful to troubleshoot mods. 

**Continue**
- (Optional) Enable *Hide Credits Button* and *Hide New Game Button (In Game)*.

**Improved Vanilla Leveling**
- Enable *Enhanced Tooltip*. This option assumes you haven't installed the "Level-up skills tooltip" patch in the Morrowind Code Patch.

**Let There Be Darkness - Lua Lighting Overhaul**
- In the **General and Cell Settings** tab, set *Cell lighting value overrides* to *NONE*.
- If you've installed the specialprocess shader in **Setup**, set all three *Ambient color adjustments* to *75*.
- In the **Light Settings** tab, disable *Use TLaD overrides for radius and color of light sources?*.

**UI Expansion**  
Please bear in mind that your game *may* crash when configuring this mod. That said, whatever changes you made will persist after running the game again.

- Set *Auto-select search bar* to *None*. I found this option to be particularly annoying as I would accidentally press one of my movement keys after opening the menu, and suddenly one of my search bars would be filtered.
- (Optional) Set *Use verbose buttons instead of icons for inventory filtering?* to *No*.
- (Optional) Set *Use search bars?* to *No*.

### MOD KEYBINDINGS

The mods installed in this guide and configured as mentioned above will use the following keys:

- **Security Enhanced**: **L** key to equip lockpicks, **P** key to equip probes.
- **Torch Hotkey**: **C** key to equip light sources.

[<< Back to Main](https://github.com/Sigourn/morrowind-improved/blob/master/readme.md#morrowind)  
[<< Back to Setup](https://github.com/Sigourn/morrowind-improved/blob/master/setup.md#setup)
