# MORROWIND#

Version 2.4.0 (March 2nd)

[<< Back to Main](https://github.com/Sigourn/morrowind-improved/blob/master/readme.md#morrowind)  
[<< Back to Setup](https://github.com/Sigourn/morrowind-improved/blob/master/setup.md#setup)

## INDEX

- [Changelog](https://github.com/Sigourn/morrowind-improved/blob/master/mw2.md#changelog)
- [Introduction](https://github.com/Sigourn/morrowind-improved/blob/master/mw2.md#introduction)
  - [Following the setup guide](https://github.com/Sigourn/morrowind-improved/blob/master/mw2.md#following-the-setup-guide)
  - [Modding tips](https://github.com/Sigourn/morrowind-improved/blob/master/mw2.md#modding-tips)
  - [The Overwrite folder](https://github.com/Sigourn/morrowind-improved/blob/master/mw2.md#the-overwrite-folder)
- [Core module](https://github.com/Sigourn/morrowind-improved/blob/master/mw2.md#core-module)
- [UI and Hotkeys module](https://github.com/Sigourn/morrowind-improved/blob/master/mw2.md#ui-and-hotkeys-module)
- [Visuals module](https://github.com/Sigourn/morrowind-improved/blob/master/mw2.md#visuals-module)
- [Audio module](https://github.com/Sigourn/morrowind-improved/blob/master/mw2.md#audio-module)
- [Dialogue and Quests module](https://github.com/Sigourn/morrowind-improved/blob/master/mw2.md#dialogue-and-quests-module)
- [Gameplay module](https://github.com/Sigourn/morrowind-improved/blob/master/mw2.md#gameplay-module)
- [Finishing touches](https://github.com/Sigourn/morrowind-improved/blob/master/mw2.md#finishing-touches)
  - [Morrowind Code Patch](https://github.com/Sigourn/morrowind-improved/blob/master/mw2.md#morrowind-code-patch)
  - [Install order and load order](https://github.com/Sigourn/morrowind-improved/blob/master/mw2.md#install-order-and-load-order)
  - [Synchronizing mod masters](https://github.com/Sigourn/morrowind-improved/blob/master/mw2.md#synchronizing-mod-masters)
  - [Plugin cleaning](https://github.com/Sigourn/morrowind-improved/blob/master/mw2.md#plugin-cleaning)
  - [Conflict resolution](https://github.com/Sigourn/morrowind-improved/blob/master/mw2.md#conflict-resolution)
  - [Running Distant Land](https://github.com/Sigourn/morrowind-improved/blob/master/mw2.md#running-distant-land)
  - [Closing comments](https://github.com/Sigourn/morrowind-improved/blob/master/mw2.md#closing-comments)
- [In-game configuration](https://github.com/Sigourn/morrowind-improved/blob/master/mw2.md#in-game-configuration)
- [Mod keybindings](https://github.com/Sigourn/morrowind-improved/blob/master/mw2.md#mod-keybindings)
- [Credits](https://github.com/Sigourn/morrowind-improved/blob/master/mw2.md#credits)
- [Compatibility](https://github.com/Sigourn/morrowind-improved/blob/master/mw2.md#compatibility)

## CHANGELOG

<details>
  <summary>v2.4.0</summary>

With this update, a new game is recommended.

- Added Expansion Delay (Dialogue and Quests).
- Removed LDM - Choices and Consequences. After thoroughly looking at the changes from the mod, I noticed that the ones I would like to keep aren't that many themselves. Adding the individual mods to the guide itself feels fairly pointless as well.
- Removed Hospitality Papers Expanded. I would like to avoid adding dialogue mods when possible.
- Removed Tunnel Cough. It really wasn't worth it.
</details>

## INTRODUCTION

### Following the Setup guide

The guide presented here assumes you have already followed the installation instructions found in the [**Setup**](https://github.com/Sigourn/morrowind-improved/blob/master/setup.md#setup) page. Please abstain from using this guide until you've correctly set up Morrowind.

Unlike Morrowind++ (which Morrowind# is an extension and a slight rework of), this guide assumes a certain level of competence from its users, and knowledge about the game. Because of this, instructions have been simplified, particularly those that always pointed out when Mod Organizer 2 won't recognize a mod's Data Files structure.

### Modding tips

**Mod Organizer 2** lets you hide specific files from your installed mods, including anything from meshes to textures, but also plugins. This is a especially useful feature when you deactivate certain plugins from a mod but don't want to see them cluttering up your load order, or you want certain files not to overwrite another mod's.

- To hide a plugin, right click on your installed mod and click **Information...**.
- On the **Filetree** tab, right click on the plugins, folders, or files you want to hide, and click **Hide**.

Mod Organizer 2 will hide the files, and these will no longer affect your game.

### The Overwrite folder

The **Overwrite** folder is the destiny folder for the output of many of the tools we installed in **Setup**, e.g. distant Land generation will place its contents inside the **distantland** folder, configurable MWSE mods will place their files inside the **MWSE\config** folder. There's always a chance files in the **Overwrite** folder will overwrite assets and/or plugins from your installed mods.

## CORE MODULE

### Bug fixes and optimization

- [**Patch for Purists**](https://www.nexusmods.com/morrowind/mods/45096) by half11  
The best unofficial fan patch for Morrowind.
- [**Unofficial Morrowind Official Plugins Patched**](https://www.nexusmods.com/morrowind/mods/43931?) by PikachunoTM  
Includes fixes for all of the Official Plugins.
  - Install **UMOPP 3.1.0** only.
  - Hide all plugins except *bcsounds.ESP* and *master_index.ESP*
- [**Correct UV Rocks**](http://mw.modhistory.com/download-56-12003) by Nich  
Fixes UV mapping on rocks and stones.
- [**Morrowind Optimization Patch**](https://www.nexusmods.com/morrowind/mods/45384?) by Remiros and Greatness7  
Greatly improves performance and fixes some mesh errors.
  - In the BAIN installer, tick the following options only:
    - **00 Core**
    - **01 Fixed Vanilla Textures**
    - **02 Lake Fjalding Anti-Suck**
    - **03 MGE XE Addon**
    - **05 Chuzei Fix**
  - Hide **meshes\f\furn_web10.nif**. This mesh causes a certain cobweb to lose transparency at a distance when using Intelligent Textures (present in this guide).
- [**Project Atlas**](https://www.nexusmods.com/morrowind/mods/45399) by the Project Atlas Team  
Optimizes the most performance heavy areas of vanilla Morrowind through texture atlases. 
  - In the BAIN installer, tick **00 Core** only.
  - Hide **meshes\x\ex_imp_plat_01.nif**. This mesh is buggy and can cause problems when traveling from Raven Rock to Fort Frostmoth using the boat.
- [**Creature VFX Restoration**](https://www.nexusmods.com/morrowind/mods/46194?) by rot  
Restores visual effects on creatures. Most creature particle effects weren't displayed for technical reasons.
- [**Fix Those Bastard Rope Fences**](https://www.nexusmods.com/morrowind/mods/45741) by EJ-12 and Petethegoat  
Modifies collision boxes on rope-related meshes, player and NPC's hitboxes to prevent getting stuck.
- [**Glowing Flames**](https://www.nexusmods.com/morrowind/mods/46124) by PoodleSandwich  
Flames are now glow mapped and/or properly illuminated.
  - Install **Glowing Flames** only.
  - Hide *Glowing Flames - TrueLightsAndDarkness Tweaks.ESP*
- [**Silt Strider Animation Restored**](https://www.nexusmods.com/morrowind/mods/44150?) by R-Zero  
Restores previously unused Silt Strider animation - it was present in the model, but never played in the game itself because of the lack of the necessary script. It also comes with a previously unused sound.
- [**Expeditious Exit**](https://www.nexusmods.com/morrowind/mods/45634) by NullCascade  
Forces the game to instantly close on exit.
- [**Quest Skill Reward Fix**](https://www.nexusmods.com/morrowind/mods/48269) by Merzasphor  
Makes the game treat skill increases from quests as if there were raised via normal means, solving numerous problems with how the game treats these skill increases.
- [**Skill Increase GMST Fix**](https://www.nexusmods.com/morrowind/mods/48029) by Merzasphor  
Fixes several engine bugs related to GMSTs used when raising skills via NPC training and skill books.

### Non-purist fixes

- [**Immersive Run Fix**](https://www.nexusmods.com/morrowind/mods/45947) by Petethegoat  
Normalizes the player's movement speed, ensuring they run at a consistent speed even during diagonal movement.
- [**Divayth Fyr Puzzle Fixed**](https://www.nexusmods.com/morrowind/mods/45155) by Remiros  
Reworks Divayth Fyr’s puzzle so that you require the correct key to open the chests as well as locking up all the artifacts, which now require the final key to be opened.
- [**Dubdilla Location Fix**](https://www.nexusmods.com/morrowind/mods/46720) by half11  
Moves the entrance to the cavern of Dubdilla to a more logical place according to in-game information.
- [**Loading Doors Lock Tune**](https://www.nexusmods.com/morrowind/mods/46094) by abot  
Automatically synchronizes linked doors locked/unlocked state on activate, lock/unlock by spell, unlock by lockpick, key. Makes loading doors play close sound a short time after opening.
- [**Services Restored**](https://www.nexusmods.com/morrowind/mods/47068?) by half11  
Adds the missing master trainer for Medium Armor, Cinia Urtius.
  - In [**TESAME**](https://github.com/Sigourn/morrowind-improved/blob/master/mwtools.md#tesame), delete the following records: 
    - NPC **hecerinde**
  - This omits the restoration of Hecerinde's Secret Master tools.
- [**The Publicans**](https://www.nexusmods.com/morrowind/mods/45410?) by half11  
Fixes several places in the vanilla game that are set up like inns, but in which Bethesda for some reason forgot to add the option to rent a room in.

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
  - Place **daedric_font.fnt** and **daedric_font_obw.tex** in **Data Files\Fonts**.
- [**Better Dialogue Font**](https://www.nexusmods.com/morrowind/mods/36873) by Hrnchamd  
High resolution replacer for the Magic Cards font, used in most of the user interface.
  - Install **Better Dialogue Font** only.
- [**Chocolate UI**](https://www.nexusmods.com/morrowind/mods/43076/) by Innicin  
Modernizes the user interface.
  - Note that this mod includes **Better Dialogue Font**. However, because this mod is not a straight improvement over the vanilla UI (since it changes the aesthetic) I'm still listing Better Dialogue Font above should you wish to skip installing this mod.
- [**Comrade Raven's Book Arts Replacer**](https://www.nexusmods.com/morrowind/mods/48896?) by Alfred Khamidullin and Comrade Raven  
Replaces most of original book arts with hi-res images redrawn from scratch by Alfred “Hieronymus7Z” Khamidullin.
- [**Pete's Scroll 2018 ...in 2020**](https://www.nexusmods.com/morrowind/mods/47863/?) by Petethegoat  
Replacement scroll and journal textures, rendered out in 1k, 2k, and 4k dimensions.
  - Install **Pete's Journal and Scroll** only.
    - In the BAIN installer, tick **01 Journal and Scroll - 2K** only.
- [**Title Screen and Logo Video Intro Reworked**](https://www.nexusmods.com/morrowind/mods/43657) by Phobos  
HD recreation of the Title and Logo Intro, in widescreen.
  - Install **Title Screen Reworked (Widescreen)** only (assuming you enabled *Skip opening movie* in MGE XE).
- [**Widescreen Splash Replacer**](https://www.nexusmods.com/morrowind/mods/47163) by NZdawghaus  
Replaces the default splash screens with better quality widescreen versions (16:9), and adds three missing Bethesda splash screens.
- [**Widescreen Splash Additions**](https://www.nexusmods.com/morrowind/mods/48001) by Tixen  
Adds the three missing Bethesda splash screens not covered by NZdawghaus' mod in widescreen resolution.
  - Place the loose .tga files in **Data Files\Splash**.

### UI

- [**Better Questlist**](https://www.nexusmods.com/morrowind/mods/48272) by Virnetch  
Allows highlighting and hiding quests in the Journal questlist. Shift-Click on a quest to highlight it, Shift-Click again to hide and Shift-Click a third time to return to normal.
- [**Book Worm**](https://www.nexusmods.com/morrowind/mods/46851) by Merlord  
Keep track of what books you have read by showing a "(Read)" indicator next to their names. You can also see a list of previously read books in the MCM menu.
- [**Class Description Tooltip**](https://www.nexusmods.com/morrowind/mods/47527) by Merlord  
Restores the description tooltip to the vanilla class selection menu.
- [**Clock Block**](https://www.nexusmods.com/morrowind/mods/46292) by Aleist3r  
Adds clock to UI that displays either game world time or real time (depending on settings).
- [**Companion Health Bars MWSE Lua Script**](https://www.nexusmods.com/morrowind/mods/46136) by mesafoo  
Adds health bars for your companions and summoned creatures to the Morrowind HUD. 
- [**Consistent Keys**](https://www.nexusmods.com/morrowind/mods/47954) by Necrolesian  
Renames keys so they'll have a consistent naming scheme.
  - Install **MWSE Version** only.
- [**Continue**](https://www.nexusmods.com/morrowind/mods/45952?) by Petethegoat  
Adds a continue button to the main menu to instantly load your most recent save.
- [**Essential Indicators**](https://www.nexusmods.com/morrowind/mods/48267) by Anumaril21  
Provides configurable, dynamic crosshair indicators while sneaking and for essential NPCs, quest items, owned objects, and more. In addition, a variety of settings are included to manage how these aspects of the game work. 
- [**HUD Weapon Charge**](https://www.nexusmods.com/morrowind/mods/47962) by Virnetch  
Adds a fillbar that shows the currently equipped weapon's charge under the weapon condition bar on the HUD.
- [**Memory Monitor**](https://www.nexusmods.com/morrowind/mods/45696) by NullCascade  
Provides an in-game HUD element as the game approaches critical memory limits. At a critical threshold, it can prompt to save and quit.
- [**New Game Confirmation**](https://www.nexusmods.com/morrowind/mods/47693?) by hardek  
Adds a confirmation popup when you click on New Game in the main menu.
- [**Shrine Tooltips**](https://www.nexusmods.com/morrowind/mods/48275) by Virnetch  
Adds tooltips with the effect's name to shrines when hovering over the different options.
- [**Smart Ammo**](https://www.nexusmods.com/morrowind/mods/47383?) by abot  
Ammo autoequip while bow/crossbow/thrown weapon readied. It will remember and prefer last hand-picked ammo if pressing Alt while equipping it.
  - Requires [**MWSEabotlib**](https://www.nexusmods.com/morrowind/mods/47717) by abot.
- [**Smart Journal**](https://www.nexusmods.com/morrowind/mods/47492?) by abot  
Adds several new options for the journal and quest pages.
- [**Smart Map**](https://www.nexusmods.com/morrowind/mods/46634) by abot  
Automatically switches between the local and world map depending on user configuration.
  - Requires [**MWSEabotlib**](https://www.nexusmods.com/morrowind/mods/47717) by abot.
- [**Tooltip**](https://www.nexusmods.com/morrowind/mods/45969) by abot  
Displays Value/Weight Ratio of currently focused object/inventory item in tooltip. Display of Skillbook teached skill and mod source may also be enabled from the MCM control panel.
- [**UI Expansion**](https://www.nexusmods.com/morrowind/mods/46071?) by NullCascade  
Expands UI functionality with searching, filtering, and more visual feedback.

### Hotkeys

- [**Book Pickup**](https://www.nexusmods.com/morrowind/mods/46625) by NullCascade  
Enables picking up books by default, instead of opening them. This can be disabled by holding shift. The behavior can be inverted using the mod config menu.
- [**Hotkeys Extended**](https://www.nexusmods.com/morrowind/mods/48055) by Virnetch  
Expands the vanilla Quick Menu by adding different hotkeys for holding or double tapping a button and/or when holding a specific button. All hotkeys use the same keys as in vanilla. In total there can now be 81 different hotkeyed items/spells.
- [**Hot Quests**](https://www.nexusmods.com/morrowind/mods/48976) by abot  
Adds hotkeys for journal Quests and Topics.
- [**Kill Command**](https://www.nexusmods.com/morrowind/mods/46723) by Merlord  
Adds a configurable hotkey that will send all companions to attack whatever you are currently looking at.
- [**Quick Equip**](https://www.nexusmods.com/morrowind/mods/48341) by Merlord  
Holding down a hotkey (default left shift) while clicking an item in your inventory will equip that item instead of picking it up. 
- [**Right Click Menu Exit**](https://www.nexusmods.com/morrowind/mods/48458) by Merlord  
Exit any menu by right clicking (or whatever your menu key is mapped to).
- [**Security Enhanced**](https://www.nexusmods.com/morrowind/mods/47038) by OperatorJack  
Adds hotkeys for lockpicks and probes, as well as hotkey cycling options, ordering options, and auto-equip options for activating locked or trapped objects.
- [**Switchable Scriptures**](https://www.nexusmods.com/morrowind/mods/46680) by Stuporstar and NullCascade  
Lets you open or close any book or scroll in the game.
  - In the BAIN installer, tick **00 Core** and **01 Closed Book Icons** only.
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
- [**Distant Mournhold**](https://www.nexusmods.com/morrowind/mods/43255) by EnvyDeveloper  
Adds distant buildings to Mournhold, letting you see the temple from almost any part of the city. 
- [**Hidden Imperial Door Fix**](https://www.nexusmods.com/morrowind/mods/43528?) by Melchior Dahrk  
Gives the hidden imperial door the same shading as the walls it is next to so that it doesn't stick out like a sore thumb.
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
- [**Well Diversified**](https://www.dropbox.com/sh/7fv2wojbp6y3uo9/AABIH_hMYjbqmZCPBnyu4NPqa?dl=0&preview=Well+Diversified.7z) by Slartibartfast  
Creates variants of the well mesh to better fit Imperial and Solstheim architecture.
  - Place the **x** folder in **Data Files\Meshes**.

### Equipment and Items

- [**Arukinns Better Books and Scrolls**](https://www.nexusmods.com/morrowind/mods/43100) by Arukinn  
Replaces all the books, bookpages and scrolls.
  - I recommend hiding all textures beginning with **Tx_book_pages_**, as they tend to display Christian iconography unfit for Morrowind.
- [**Bloodmoon Hide Replacer BHR**](https://www.nexusmods.com/morrowind/mods/21725?) by Alaisiagae  
Mesh and texture replacer for the Bear, Snow Bear, Wolf, and Snow Wolf ingredients so that they look like pelts instead of mutilated heads.
- [**Complete Armor Joints**](http://mw.modhistory.com/download-4-12572) by Kahkahra  
Adds the unused forearm joint to the Orcish Pauldrons, Dwemer Pauldrons, and the three types of Bonemold Pauldrons, and modifies the Dwemer, Daedric, Chitin and Netch greaves and pauldron to prevent them showing clothing underneath.
- [**Imperial Steel Cuirass With Belt**](https://www.nexusmods.com/morrowind/mods/49232) by Quorn and Alaisiagae  
Mesh replacer that adds the missing belt to the male Imperial Steel Cuirass.
- [**Improved Nordic Iron Helm**](https://www.nexusmods.com/morrowind/mods/43816/) by Daemonjax  
Mesh replacer for the Nordic Iron Helm mesh that adjusts its proportions.
  - Install **Improved Nordic Iron Helm 1.0-alternate** only.
- [**Improved Thrown Weapon Projectiles**](https://www.nexusmods.com/morrowind/mods/44763?) by R-Zero  
Mesh replacer for thrown weapon projectiles that makes them fly pointy end forward and, in some cases, spin in the air.
- [**Melchior's Magnificent Manuscripts**](https://www.nexusmods.com/morrowind/mods/45626) by Melchior Dahrk  
Model replacer for all of the vanilla books.
  - In the BAIN installer, tick **00 Core** only.
  - Also install [**Switchable Scriptures**](https://www.nexusmods.com/morrowind/mods/46680) Melchior's Magnificent Manuscripts Patch. 
    - In the BAIN installer, tick **03 Melchior's Magnificent Manuscripts** only. Rename the mod to **Switchable Scriptures - Melchior's Magnificent Manuscripts Patch**.
- [**No Orcish Clown Shoes**](https://www.nexusmods.com/morrowind/mods/45939) by Petethegoat  
Mesh replacer that reduces the dimensions and spikiness of Orcish Boots.
- [**Snow Prince Armor Redux (MMC Edit)**](https://www.nexusmods.com/morrowind/mods/49232) by Saint_Jiub, Moranar, and Sigourn  
Remodel and retexture of the Ancient Steel Armor set found in Bloodmoon.
- [**Soldier Belts Fix**](https://www.nexusmods.com/morrowind/mods/25556) by Alaisiagae  
Gives the Templar, Imperial, and Indoril Belts unique meshes and icons.
- [**Weapon Sheathing**](https://www.nexusmods.com/morrowind/mods/46069) by TES3 Community
Equipped weapons will be shown on the character's hip or back. This new functionality affects both the player and all other characters, and works with all weapons from all mods. Additionally features a comprehensive set of high quality quiver and scabbard assets.
  - Install **WeaponSheathing 1.6-MWSE** only.
  - Also install [**Weapon Sheathing - Bow Position Edit**](https://www.nexusmods.com/morrowind/mods/48473?) by Kyim. The bows will better line up with the sheathing animation.
  - Also install the [**Morrowind Optimization Patch**](https://www.nexusmods.com/morrowind/mods/45384?) Weapon Sheathing Patch.
    - In the BAIN installer, tick **04 Weapon Sheathing Patch** only. Rename the mod to **Morrowind Optimization Patch - Weapon Sheathing Patch**.
- [**Wolf Helmet Replacer**](https://www.nexusmods.com/morrowind/mods/29281) by Alaisiagae  
Mesh and icon replacer for the Wolf and Snow Wolf Helmets with a ferocious wolf head with gaping jaws.

### NPCs and Creatures

- [**Buoyant Lord Vivec**](https://www.nexusmods.com/morrowind/mods/48312) by Stripes  
Adds a simple script to make Vivec properly loop his idle animation.
  - In the BAIN installer, tick **00vanilla** only.
- [**Golden Saint Feminine Walk**](https://www.nexusmods.com/morrowind/mods/42703?) by dopey fish  
Gives the base golden saint the feminine walk animation instead of the default male walk animation.
  - Place **XGolden Saint.kf** and **XGolden Saint.nif** in **Data Files\Meshes\r**.
- [**Incarnates Overhauled (Sigourn Edit)**](https://www.nexusmods.com/morrowind/mods/49232) by Aoimevelho and Sigourn  
Changes the armor and clothes of some of the ghosts, so that now an ashlander wears ashlander clothes, a warrior of the Temple wears Indoril armor, Erur-Dan wears his cuirass, Hort-Ledd wears his robe, and so on.
- [**Yet Another Guard Diversity**](https://www.nexusmods.com/morrowind/mods/45894) by Half11, SkoomaPro, and Danke  
Replaces the generic, copy-pasted guards of Morrowind with different variations. Some guards have different loadouts and armor, and each have different faces. Note that guards added by other mods will use the generic default guards.

### VFX

- [**Flies**](https://www.nexusmods.com/morrowind/mods/43481) by R-Zero  
Adds a visual effect to all vanilla flies sound emitters. Now everywhere you can hear flies buzzing, you'll be able to actually see fly swarms too.
  - Also install [**Flies Fixed**](https://cdn.discordapp.com/attachments/218457935846703104/803267311246245908/Flies.ESP) by ProfArmitage, which fixes flies appearing underwater.
- [**Glow in the Dahrk**](https://www.nexusmods.com/morrowind/mods/45886) by Melchior Dahrk and NullCascade  
Makes windows glow in the dark.
  - In the FOMOD installer, install the following options:
    - Interior Sunrays.
    - Nord Glass Windows.
    - Raven Rock Glass Windows.
    - Hi-Res Window Texture Replacer.
  - Also install the [**Project Atlas**](https://www.nexusmods.com/morrowind/mods/45399) Glow in the Dahrk Patch.
    - In the BAIN installer, tick **10 Glow in the Dahrk Patch - Interior Sunrays** only. Rename the mod to **Project Atlas - Glow in the Dahrk Patch**.
- [**Mistify**](https://www.nexusmods.com/morrowind/mods/48112) by Melchior Dahrk  
Replaces the vanilla mist effect.
  - In the BAIN installer, tick **01 vanilla mist replacer** only.
  - The complete mod is incompatible with **Bitter Coast Scum Replacer**.
- [**Mist Retexture**](https://www.nexusmods.com/morrowind/mods/44322) by Remiros  
Improves the texture for the mist. The mist is now much smoother and more detailed, as well as less opaque and flat. This also makes it play much nicer with SSAO.
  - Install **Mist Retexture** only.
- [**MWSE Blood Diversity**](https://www.nexusmods.com/morrowind/mods/47913) by Anumaril21  
Provides a variety of new configurable blood types for the creatures of Morrowind, Tribunal, Bloodmoon, the Official Plugins, and a variety of mods.
  - In the BAIN installer, tick **00 Core** and **02 R-Zero's Textures** only.
  - This mod requires additional Morrowind.ini configuration. Follow the instructions on the mod's page.
- [**No Shield Sparkle**](https://www.nexusmods.com/morrowind/mods/45989?) by jiopi  
Removes the annoying sparkle effects from Shield.
- [**Subtle Magic Glow**](https://www.nexusmods.com/morrowind/mods/4468?) by atteSmythe  
Replaces the "plastic wrap" effect around in-game magic items (those equipped by characters or on the ground) with less-obtrusive versions.
  - In the BAIN installer, tick **faint** only.
- [**Subtle Smoke**](https://www.nexusmods.com/morrowind/mods/47341) by wazabear  
Makes it so many smoke effects are much more laid back and easier on the eyes.
- [**The Dream is the Door**](https://www.nexusmods.com/morrowind/mods/47423) by Melchior Dahrk  
To align with what the in game dialogue suggests, the entrance to the Cavern of the Incarnate will now only be visible during the magical hours of twilight.
- [**Visually Filled Soul Gems**](https://www.nexusmods.com/morrowind/mods/46709) by NullCascade  
Makes in-world soul gems that are filled appear as enchanted items.

### Weather and Lighting

- [**Apel's Rain Replacer**](https://www.nexusmods.com/morrowind/mods/42555) by Apel and HedgeHog-12  
Replaces rain with a more heavy rain look.
- [**Let There Be Darkness - Lua Lighting Overhaul**](https://www.nexusmods.com/morrowind/mods/47912/) by Greatness7, Merlord, OperatorJack, Petethegoat, and RedFurryDemon  
Configurable mod for automatical adjustment of lighting, including override values, cell whitelist, and light object editing.
  - Also install the [**No Level Design Lighting Preview Patch**](https://www.mediafire.com/file/5vidcblah6g4tcy/Let+There+Be+Darkness+(No+Level+Design+Lighting+Preview+Patch).zip/file), which solves a compatibility issue with mods that use the **L** as a hotkey, such as Security Enhanced. Make sure you only install this mod for version 1.1 of Let There Be Darkness.
- [**Light Decay**](https://www.nexusmods.com/morrowind/mods/46671) by Greatness7 and Melchior Dahrk  
The radius of a handheld light will gradually diminish and eventually go out when the light extinguishes.
- [**Transporter Lights**](https://www.nexusmods.com/morrowind/mods/48050) by Eq  
Caravaners, Gondoliers, and Shipmasters equip lights at night for more immersion.
- [**Weather Adjuster**](https://www.nexusmods.com/morrowind/mods/46816) by Hrnchamd  
Regional weather colours, skies and lighting. Visual weather editor and region-based presets. Seamless transitions between regions.
  - This mod lets you adjust many variables about Morrowind's weather. Read the description to learn how to do this. The reason I recommend it (aside because of how great the mod is) is that users can share their presets: the mod on its own will not change the appearance of the game until you configure it so.
  - Also install [**Weather Adjuster - Morrowind++ Preset**](https://www.mediafire.com/file/1fqz9ovi69chkgp/Weather+Adjuster+-+Morrowind+++Preset+v2.1.zip/file). Personal preset for darker nights and less horrible fog.
    - This mod has to be installed manually. Unpack the file and merge the **overwrite** folder with your Mod Organizer 2 **overwrite** folder, found inside the **Mod Organizer 2** folder. The contents of the folder should like so: **Mod Organizer 2\overwrite\MWSE\config\Weather Adjuster.json**.
    - [**Comparison here.**](https://imgsli.com/MTUwMjI)

## AUDIO MODULE

- [**Heartthrum**](https://www.nexusmods.com/morrowind/mods/47178) by RedFurryDemon and OperatorJack  
Allows you to hear the beating Heart of Lorkhan all the way to the exterior of the Dagoth Ur citadel.
- [**No Female Nord Screeching**](https://www.nexusmods.com/morrowind/mods/49232) by Sigourn  
Replaces a handful of sound files to stop female Nords from bursting your ear drums when they are attacked.
- [**Outdoor Banners With Sound**](https://www.nexusmods.com/morrowind/mods/47068) by Half11  
Outdoor banners now play sound alongside their animations. The sounds are noticeable, but not overly loud.
- [**Sheep-no-More**](https://www.nexusmods.com/morrowind/mods/45168) by McChuggernaut  
Removes the sheep sounds from Morrowind.
- [**Shut the Fuck up Cliff Racers**](https://www.nexusmods.com/morrowind/mods/46588) by Merlord  
Drastically reduces the frequency of idle Cliff Racer screeches, by editing the kf file of the cliff racer mesh.
- [**Silent Assassins**](https://www.nexusmods.com/morrowind/mods/44371) by R-Zero  
Assassin class NPCs will be 10 times less likely to grunt or taunt you in combat.
- [**Sound Spell Sound Effect**](https://www.nexusmods.com/morrowind/mods/43300) by R-Zero  
With this plugin the player can hear an actual noise when he's under the effects of the Sound magic.
- [**Water Sounds**](https://www.nexusmods.com/morrowind/mods/47794) by abot  
Simulates water sounds when colliding with generic fake animated water meshes.

## DIALOGUE AND QUESTS MODULE

- [**Early Transport to Mournhold**](https://www.nexusmods.com/morrowind/mods/47985) by Necrolesian  
Allows travel to Mournhold before the Dark Brotherhood attacks begin.
- [**Expansion Delay**](https://www.nexusmods.com/morrowind/mods/47588) by Half11  
- Fixes Bethesda's overly enthusiastic expansion hooks by delaying the Dark Brotherhood attacks (for Tribunal) and limiting intrustive dialogue topics to a few NPCs (Bloodmoon).
- [**FMI - NotAllDunmer**](https://www.nexusmods.com/morrowind/mods/47569) by PoodleSandwich  
Not all Dunmer are slavers. Not all Argonians are slaves. Idle dialogue filtering has been improved to reflect this.
- [**Great Service**](https://www.nexusmods.com/morrowind/mods/47767) by Von Djangos  
Enables over 100 lines of voiced dialogue for shopkeepers that were shipped with the original game but never used.
- [**Greetings for No Lore**](https://www.nexusmods.com/morrowind/mods/46063) by Caeris  
Replaces the three standard No Lore greetings with over sixty new ones.
- [**Idle Talk**](https://www.nexusmods.com/morrowind/mods/46948) by Von Djangos  
Adds over 200 new voice entries for NPCs, mostly using edited original voice files.
- [**Its a Deal**](https://www.nexusmods.com/morrowind/mods/47968) by Petethegoat and Von Djangos  
Shopkeepers will now comment with a line of voiced dialogue on a successful trade.
- [**LDM - Context Matters**](https://www.nexusmods.com/morrowind/mods/48273) by Lucevar  
Edits, re-filters, or adds on to vanilla dialogue to add more situational nuance.
- [**Outfit Greetings Tweaked**](https://www.nexusmods.com/morrowind/mods/46066) by Anille  
Greetings regarding clothes are limited to clothiers, nobles and snooty High Elves.

## GAMEPLAY MODULE

### Quality of life improvements

- [**Adamantium Ore Fix**](https://www.nexusmods.com/morrowind/mods/47068?) by Half11  
Allows the player to find the exact amount of Adamantium Ore needed to craft Bols Indalen's custom Adamantium Armor.
- [**Bed Buddies**](https://www.nexusmods.com/morrowind/mods/46632) by Merlord  
Prevents you from sleeping in owned beds unless the owner really likes you. Attempting to sleep in an owned bed no longer triggers a crime, even if the owner doesn't like you.
- [**Better Propylon Teleport Script**](https://www.nexusmods.com/morrowind/mods/46364) by PikachunoTM  
The Warp Script for the Propylon Indices will now prompt you before teleporting. The Master Index version additionally lets you choose your destination when warping if you have the Master Index in your possession.
  - Hide *Better Propylon Teleport Warp.ESP*
- [**Diligent Defenders**](https://www.nexusmods.com/morrowind/mods/45717?) by NullCascade  
When the player or the player's companions are attacked, any companions will launch into action in defense.
- [**Easy Escort**](https://www.nexusmods.com/morrowind/mods/45712?) by NullCascade  
Ensures that your followers get warped to you if they get too far away. Compatible with any follower from any mod, without any special script attached to that NPC.
- [**Gondolier Destinations**](https://www.nexusmods.com/morrowind/mods/42306) by PeterBitt  
Each gondolier in Vivec will get you to all gondolier ports in Vivec.
- [**Graphic Herbalism - MWSE Edition**](https://www.nexusmods.com/morrowind/mods/46599) by Stuporstar and Greatness7  
Automatically harvests herbs, instead of opening the container interface. Picked herbs will now have their meshes modified or disappear altogether (they will still respawn).
  - In the BAIN installer, tick **00 Core + Vanilla Meshes** only.
  - Also install **GH Patches and Replacers**.
    - In the BAIN installer, tick **10 Atlas - Vanilla BC Mushrooms** only.
  - Also install [**Graphic Herbalism Lighting**](https://www.nexusmods.com/morrowind/mods/47864), which makes picking a glowing plant also remove the glow-light.
- [**MWSE Hide the Skooma**](https://www.nexusmods.com/morrowind/mods/48454) by Necrolesian  
Automatically hides your drugs so you don't have to dump them on the floor in order to trade.
- [**Pluginless and Adjustable Lower First Person Sneak**](https://www.nexusmods.com/morrowind/mods/48642) by Celediel  
Lowers the position of the first person camera when sneaking/crouching, making it easier to tell if you are sneaking. Adjustable on the fly.
- [**Temples With Shrines**](https://www.nexusmods.com/morrowind/mods/45535?) by Leyawynn  
There are numerous temples that don't have any shrines inside. This mod adds shrines to the temples in Maar Gan, Molag Mar, Suran and Vos.
- [**Wading in Water MW**](https://www.nexusmods.com/morrowind/mods/48783) by R-Zero  
Slows all creatures, NPCs and the Player down when they are walking half-submerged in water.

### Leveling/Attributes/Skills tweaks

- [**Class-Conscious Character Progression (CCCP)**](https://www.nexusmods.com/morrowind/mods/48110) by Necrolesian  
An MWSE leveling mod that implements most features of Galsiah's Character Development. I strongly recommend you read the mod's page.
- [**Cost Based Enchant Progression**](https://www.mediafire.com/file/udrqcrzrz9uatxz/Cost_Based_Enchant_Skill_Progression_v1.0.zip/file) by Greatness7 and Sigourn  
Enchant skill advances based on the cost of the enchantment cast, calculated as if it was a spell.
- [**Hold Your Breath**](https://www.nexusmods.com/morrowind/mods/48872) by Stripes  
Endurance determines how long you can hold your breath under water. Uses MWSE.
- [**Magicka Based Skill Progression**](https://www.nexusmods.com/morrowind/mods/48330) by JaceyS  
Spellcasting skills advance based on the amount of Magicka spent, rather than the number of spell casts.
- [**Marksman Rebalanced**](https://www.nexusmods.com/morrowind/mods/46715) by Merlord  
Takes into account the distance to target when calculating the hit chance for ranged weapons. This applies to both the player and NPCs. Crouching also provides a boost to hit chance.
- [**Putting Power In Willpower**](https://www.nexusmods.com/morrowind/mods/45742) by R-Zero  
Rebalances the willpower-based spell resist mechanic, giving all in-game actors, Player, NPCs and Creatures an ability to shrug off spells through the sheer force of will.
  - Hide *Putting Power in Willpower - Absorbonach.ESP*
- [**Wings of Will - Willpower Based Levitation Speed**](https://www.nexusmods.com/morrowind/mods/46626) by Sataniel  
Levitation speed is now based on Willpower attribute instead of Speed. Calculations are otherwise the same.

### New mechanics

- [**Blighted Blight**](https://www.nexusmods.com/morrowind/mods/48631) by Necrolesian  
Restores the possibility of contracting blight diseases while out in a blight storm.
- [**Brutal Backstabbing**](https://www.nexusmods.com/morrowind/mods/45890) by Merlord  
Introduces a backstabbing mechanic - do more damage when stabbing an enemy from behind (based on Agility/Sneak). Mod Configuration Menu includes option for Short Blades only or all weapons. Be warned - NPCs can backstab you as well!
- [**Dynamic Timescale**](https://www.nexusmods.com/morrowind/mods/48287) by Necrolesian  
Changes how quickly time passes in-game depending on where you are and what you're doing.
- [**Lua Lockbashing**](https://www.nexusmods.com/morrowind/mods/48544) by OEA  
Adds in lock-bashing from Daggerfall.
- [**Lucky Strike - A Critical Hit Mod (MMC Edit)**](https://cdn.discordapp.com/attachments/218457935846703104/803328785436115004/Lucky_Strike_-_A_Critical_Hit_Mod_v1.0_MMC_Edit.zip) by R-Zero and the Morrowind Modding Community  
Add as Luck-based Critical Strike mechanic reminiscent of one in Daggerfall.
- [**Religions Elaborated**](https://www.nexusmods.com/morrowind/mods/47843/) by Caeris  
Adds supply chests to the Imperial Cult and Tribunal Temple factions, disallows you from being a member of both factions, adds missing temple markers, and adds healing services to healers.
  - Install **No Quest Changes** only.
- [**Supply Chests**](https://www.nexusmods.com/morrowind/mods/49232) by Gavrilo93, CryptsOfTheDead, and Sigourn  
Adds supply chests to the Imperial Legion and Morag Tong factions, and adds a supply chest to the Mages Guild in Caldera.
  - In the BAIN installer, tick **01 Supply Chests (Religions Elaborated Compatible)** only.

### Equipment

- [**Area Effect Arrows Integrated**](https://www.nexusmods.com/morrowind/mods/47745) by Necrolesian  
An alternative version of the official plugin Area Effect Arrows that distributes the new projectiles throughout the game world rather than dumping them all in one shop, and includes an integrated version of BTB's Area Effect Projectiles.
  - Hide all plugins except *Area Effect Projectiles Integrated.ESP*
- [**Projectiles Reintegrated**](https://mw.moddinghall.com/file/51-projectiles-reintegrated/) by Sigourn  
Increases the availability of projectiles all over Vvardenfell, by modifying vanilla containers shared by NPCs and those specific to certain NPCs as well, in addition to adding containers of its own when more specific changes were required.
  - Install the **Vanilla Version** only.

### Balance

> Abandon all lore-friendliness, ye who enter here. *Some* of these mods contradict established lore and in-game information in their quest to rebalance the game.

- [**Controlled Consumption v1.3.0 (MMC Edit)**](https://www.nexusmods.com/morrowind/mods/49232) by NullCascade and the Morrowind Modding Community  
Provides a configurable restriction on the amount of potions and ingredients the player can drink at any one time, removing one of the largest exploits in the game.
- [**Economy Adjuster Adjustments (Crime Module)**](https://www.nexusmods.com/morrowind/mods/47130?) by HotFusion, BTB, and Necrolesian  
Increases the penalties for crime.
  - Hide all plugins except *EcoAdjCrime (Necro Edit).ESP*
- [**HardTrade (Sigourn Edit)**](https://www.mediafire.com/file/uuxqwctl9dxddax/HardTrade_v2.6_%2528Sigourn_Edit%2529.zip/file) by Archimag and Sigourn  
Eliminates trade exploits by overhauling the bartering mechanics.
- [**Limited Leaping**](https://www.nexusmods.com/morrowind/mods/46299) by NullCascade  
Puts optional restrictions on jumping, including a cooldown and/or minimum fatigue.
- [**Nimble Armor**](https://www.nexusmods.com/morrowind/mods/48251) by VitruvianGuar  
Makes armor contribute to player and NPCs' evasion modifier as well as allowing evading attacks to practice Unarmored and Light Armor skills. Unarmored will be fully focused on evading attacks (optional).
- [**No Disease Labels**](https://www.nexusmods.com/morrowind/mods/48295) by RedFurryDemon  
Removes "Diseased", "Blighted", and similar adjectives from creature names using MWSE-lua.
- [**No Rest Without Beds**](https://www.nexusmods.com/morrowind/mods/46724) by Kaedius  
Prevents the player from resting unless they activate a bed.
- [**No Taunting**](https://www.nexusmods.com/morrowind/mods/48889) by Necrolesian  
Disables the "taunt" option in the persuasion menu. This does not break the Temple quest where you have to taunt Anhaedra, because that's done with a normal dialogue topic, not through the persuasion menu.
- [**Ownership Overhaul**](https://www.nexusmods.com/morrowind/mods/48051) by Necrolesian  
Assigns ownership to the many, many items and containers that rightly should be owned but weren't, and otherwise makes adjustments to item ownership.
  - Hide/disable *Ownership Overhaul.ESP*
- [**Realistic Movement Speeds**](https://www.nexusmods.com/morrowind/mods/46248) by OperatorJack  
Modifies movement speeds when strafing or backpedalling so that they are more realistic. NPCs and player alike will no longer be able to fire volleys of arrows while running backwards to safety. Movement direction is now tactically important.
- [**Sneaky Strike**](https://www.nexusmods.com/morrowind/mods/48317) by VitruvianGuar  
Modifies critical strike coefficient depending on the weapon you use.
- [**Soulless Creatures**](https://www.nexusmods.com/morrowind/mods/49215) by akh  
Prevents souls of summoned creatures from being trapped. Configurable and expandable on other creatures. Compatible with any creature added by a mod.
- [**Morrowind Anti-Cheese - Ownership Overhaul Compatible**](https://mw.moddinghall.com/file/45-morrowind-anti-cheese-v12-ownership-overhaul-compatible/) by Remiros and Half11  
Fixes the biggest exploits and balance issues in the game.
- [**BTB's Game Improvements - Necro Edit v2.0 (Morrowind#)**](https://mw.moddinghall.com/file/40-btbs-game-improvements-necro-edit-sigourn-edit/) by BTB, Necrolesian and Sigourn  
Modified version of BTB's Game Improvements, with all modules merged, plus BTB's edits from his modified versions of Morrowind Advanced and Service Requirements, with many changes and additions.
  - In the BAIN installer, tick **00 BTBGI Necro Edit (Morrowind#)** only.
- [**Balanced Passive Races and Birthsigns**](https://www.nexusmods.com/morrowind/mods/47782) by BTB and Necrolesian  
Rebalance of races and birthsigns, based on BTB's Game Improvements, with permanent abilities in place of powers or spells.
- [**Beware the Sixth House (Sixth House Overhaul)**](https://www.nexusmods.com/morrowind/mods/46036) by mort  
Makes the Sixth House, properly, the most difficult content in the game. Intended for use with Tribunal Rebalance and Bloodmoon Rebalance.
- [**Tribunal Rebalance**](https://www.nexusmods.com/morrowind/mods/45713) by mort  
Rebalances Tribunal as if it shipped with Morrowind. Intended to be used with Beware the Sixth House.
- [**Bloodmoon Rebalance**](https://www.nexusmods.com/morrowind/mods/45714) by mort  
Rebalances Bloodmoon as if it shipped with Morrowind. Intended to be used with Beware the Sixth House.

## FINISHING TOUCHES

### Morrowind Code Patch

We have installed the Morrowind Code Patch in the **Setup** page. However, certain mods installed in this guide require specific instructions to work as intended, which is why we will be reinstalling the MCP.

Please note that you don't need to reinstall all options from scratch: the Morrowind Code Patch **remembers your previously installed options**, meaning you just need to look for the ones mentioned below and install them accordingly.

- (Game mechanics) Healthy appetite
  - Eating ingredients always succeeds, giving its first effect and skill advancement. **BTB's Game Improvements** removes the skill gain for consuming ingredients, and **Controlled Consumption (MMC Edit)** prevents you from spamming their consumption for overpowered effects.
- (Game mechanics) Attribute uncap
  - Allows levelling of the eight main attributes past 100. **Class-Conscious Character Progression** and **Balanced Passive Races and Birthsigns** benefit from the use of this patch.
- (Game mechanics) Skill uncap
  - Allows levelling of player skills past 100. **Class-Conscious Character Progression** and **Balanced Passive Races and Birthsigns** benefit from the use of this patch.
- (Mod specific) Weapon resistance change
  - Enchanted weapons no longer bypass the "normal weapon resistance" that many daedra possess. **BTB's Game Improvements** relies on this patch for its weapon resistance changes to work as intended.

### Install order and load order

The installation order dictates the priority a given mod's assets have over the mods installed before it. Respect this order to ensure assets are overwritten as intended.

<details>
<summary>Install order</summary>

- DLC: Tribunal
- DLC: Bloodmoon
- MGE XE Data Files
- MGE XE Shader - 16 Lights Shaders Alpha
- MGE XE Shader - Enhanced Water Shader 2.1 Green-Blue
- MGE XE Shader - Deband Fogaware v2
- MGE XE Shader - EdgeAA
- MGE XE Shader - Specialprocess
- Patch for Purists
- Unofficial Morrowind Official Plugins Patched
- Correct UV Rocks
- Morrowind Optimization Patch
- Project Atlas
- Creature VFX Restoration
- Fix Those Bastard Rope Fences
- Glowing Flames
- Silt Strider Animation Restored
- Expeditious Exit
- Quest Skill Reward Fix
- Skill Increase GMST Fix
- Immersive Run Fix
- Divayth Fyr Puzzle Fixed
- Dubdilla Location Fix
- Loading Doors Lock Tune
- Services Restored
- The Publicans
- Intelligent Textures
- Facelift (Meshes)
- Facelift (Textures)
- Pluginless Khajiit Head Pack - Whiskers Version
- Better Daedric Font
- Better Dialogue Font
- Chocolate UI
- Comrade Raven's Book Arts Replacer
- Pete's Scroll 2018 ...in 2020
- Title Screen Reworked
- Widescreen Splash Additions
- Widescreen Splash Replacer
- Better Questlist
- Book Worm
- Class Description Tooltip
- Clock Block
- Companion Health Bars MWSE Lua Script
- Consistent Keys - MWSE Version
- Continue
- Essential Indicators
- HUD Weapon Charge
- Memory Monitor
- New Game Confirmation
- Shrine Tooltips
- Smart Ammo
- Smart Journal
- Smart Map
- MWSEabotlib
- Tooltip
- UI Expansion
- Book Pickup
- Hotkeys Extended
- Hot Quests
- Kill Command
- Quick Equip
- Right Click Menu Exit
- Security Enhanced
- Switchable Scriptures
- Torch Hotkey
- Better Waterfalls
- Waterfalls Tweaks
- Bitter Coast Scum Replacer
- Distant Mournhold
- Hidden Imperial Door Fix
- Near Vanilla Road Sign Replacer
- Remiros' Groundcover
- Remiros' Groundcover Shaders - Landbias Fix
- Vivec Palace Water Replacer
- Well Diversified
- Arukinns Better Books and Scrolls
- Bloodmoon Hide Replacer
- Complete Armor Joints
- Imperial Steel Cuirass With Belt
- Improved Nordic Iron Helm (Alternate)
- Improved Thrown Weapon Projectiles
- Melchior's Magnificent Manupscripts
- Switchable Scriptures - Melchior's Magnificent Manuscripts Patch
- No Orcish Clown Shoes
- Soldier Belts Fix
- Weapon Sheathing
- Weapon Sheathing - Bow Position Edit
- Morrowind Optimization Patch - Weapon Sheathing Patch
- Wolf Helmet Replacer
- Buoyant Lord Vivec
- Golden Saint Feminine Walk
- Incarnates Overhauled
- Yet Another Guard Diversity - Regular
- Flies
- Flies Fix
- Glow in the Dahrk
- Project Atlas - Glow in the Dahrk Patch
- Mistify
- Mist Retexture
- MWSE Blood Diversity
- No Shield Sparkle
- Subtle Magic Glow
- Subtle Smoke
- The Dream is the Door
- Visually Filled Soul Gems
- Apel's Rain Replacer
- Let There Be Darkness - Lua Lighting Overhaul
- Let There Be Darkness (No Level Design Lighting Preview Patch)
- Light Decay
- Transporter Lights
- Weather Adjuster
- Heartthrum
- No Female Nord Screeching
- Outdoor Banners With Sound
- Sheep-no-More
- Shut the Fuck up Cliff Racers
- Silent Asssassins
- Sound Spell Sound Effect
- Water Sounds
- Early Transport to Mournhold
- Expansion Delay
- FMI - #NotAllDunmer
- Great Service
- Greetings for No Lore
- Idle Talk
- Its a Deal
- LDM - Context Matters
- Outfit Greetings Tweaked
- Adamantium Ore Fix
- Bed Buddies
- Better Propylon Teleport Script
- Diligent Defenders
- Easy Escort
- Gondolier Destinations
- Graphic Herbalism MWSE
- Graphic Herbalism - Patches and Replacers
- Graphic Herbalism Lighting
- MWSE Hide the Skooma
- Pluginless and Adjustable Lower First Person Sneak
- Temples With Shrines
- Wading in Water MW
- Class-Conscious Character Progression
- Cost Based Enchant Skill Progression
- Hold Your Breath
- Magicka Based Skill Progression
- Marksman Rebalanced
- Putting Power In Willpower
- Wings of Will - Willpower Based Levitation Speed
- Blighted Blight
- Brutal Backstabbing
- Dynamic Timescale
- Lua Lockbashing
- Lucky Strike - A Critical Hit Mod (MMC Edit)
- Religions Elaborated (No Quest Changes)
- Supply Chests
- Area Effect Projectiles Integrated
- Projectiles Reintegrated (Vanilla Version)
- Controlled Consumption (MMC Edit)
- Economy Adjuster Adjustments
- HardTrade (Sigourn Edit)
- Limited Leaping
- Nimble Armor
- No Disease Labels
- No Rest Without Beds
- No Taunting
- Ownership Overhaul
- Realistic Movement Speeds
- Sneaky Strike
- Soulless Creatures
- Morrowind Anti-Cheese - Ownership Overhaul Compatible
- BTB's Game Improvements - Necro Edit (Morrowind#)
- Balanced Passive Races and Birthsigns
- Beware the Sixth House (Sixth House Overhaul)
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
- Ownership Overhaul.esm
- Patch for Purists - Book Typos.ESP
- Patch for Purists - Semi-Purist Fixes.ESP
- bcsounds.ESP
- master_index.ESP
- Lake Fjalding Anti-Suck.ESP
- chuzei_helm_no_neck.ESP
- Glowing Flames - NoMoreLightlessFlames v1.1.ESP
- Silt Strider Animation Restored.ESP
- Divayth Fyr Puzzle Fixed.ESP
- Dubdilla Location Fix.ESP
- Services Restored.ESP
- The Publicans.ESP
- Better_Typography_Bookarts_Fix.ESP
- Waterfalls Tweaks.ESP
- Mournhold LOD.ESP
- NearVanillaRoadSigns.ESP
- Well Diversified.ESP
- Complete Armor Joints.ESP
- Buoyant Lord Vivec.ESP
- Incarnates Overhauled.ESP
- Yet Another Guard Diversity - Regular.ESP
- Flies.ESP
- GITD_WL_RR_Interiors.ESP
- The Dream is the Door.ESP
- RFD_Heartthrum.ESP
- Outdoor Banners With Sound.ESP
- Silent Assassins.ESP
- SoundSpellSoundEffect.ESP
- Early Transport to Mournhold.ESP
- Expansion Delay.ESP
- FMI_#NotAllDunmer.ESP
- Great Service.ESP
- Greetings for No Lore.ESP
- Idle Talk.ESP
- Its a deal.ESP
- LDM - Context Matters.ESP
- outfit greetings tweaked.ESP
- Adamantium Ore Fix.ESP
- Better Propylon Teleport Warp-Master Index.ESP
- PB_GondolierDestinations.ESP
- Temples With Shrines.ESP
- Religions Elaborated.ESP
- Supply Chests.ESP
- Area Effect Projectiles Integrated.ESP
- Projectiles Reintegrated.ESP
- EcoAdjCrime (Necro Edit).ESP
- Morrowind Anti-Cheese.ESP
- BTB's Game Improvements (Necro Edit).ESP
- SoldierBeltsFix.ESP
- Balanced Passive Races and Birthsigns.ESP
- Beware the Sixth House.ESP
- tribunal rebalance.ESP
- Bloodmoon Rebalance.ESP
- **Rem_AC.ESP**
- **Rem_AI.ESP**
- **Rem_AL.ESP**
- **Rem_BC.ESP**
- **Rem_GL.ESP**
- **Rem_Solstheim.ESP**
- **Rem_WG.ESP**

The plugins from **Remiros' Groundcover** should only be enabled when generating Distant Land in MGE XE, and disabled when playing the game.
</details>

### Synchronizing mod masters

Wrye Mash lets us synchronize the masters of mods we have installed. This will prevent certain error messages from popping up when launching the game.

- Run WryeMash in MO2.
- In the **Mods** tab, you will see a list with all your plugins, both active and inactive. Plugins that do not need to have their masters synchronized have a green box next to them. Those that do need to have their masters synchronized will have a box of a different color.
- Click on the faulty plugin, and a panel to the right will display the plugin's masters. Right click on either of them, and an *Update Masters* window will appear. Click *Yes*. 
- Once the window has closed, click on the *Save* button further below the same panel.

### Plugin cleaning

**tes3cmd** lets us clean all active plugins in our load order, either individually or in bulk. The latter process has the unfortunate side effect of reverting the author entry of the plugins to "tes3cmd multipatch", in addition to cleaning mods that shouldn't be cleaned (in the case of this guide, Patch for Purists). The bulk process also takes quite a while. For more information on how to clean plugins in bulk, [**check the Tools section**](https://github.com/Sigourn/morrowind-improved/blob/master/mwtools.md#tes3cmd).

For the purpose of this guide, we will only clean the plugins we know are dirty.

- Run WryeMash in MO2.
- In the **Mods** tab, right click on each of the following plugins and click *Clean with tes3cmd*. After the process is over, close the window.
  - Divayth Fyr Puzzle Fixed.ESP
  - Religions Elaborated.ESP

### Conflict resolution

**tes3cmd** also allows us to solve conflicts in leveled lists, generating a **multipatch.esp** file which will be placed at the end of our load order. This is very useful when, for example, you have a mod that adds new weapons to a leveled list while another removes items from a leveled list (such as Daedric equipment).

- Run WryeMash in MO2.
- In the **Mods** tab, click *Misc* on the header and go to **TES3cmd** -> **Create MultiPatch**.
- tes3cmd will now generate the multipatch. After the process is over, close the window. **multipatch.esp** will now be present at the end of your load order. Make sure you activate it.

**TES3Merge** lets us merge the objects in our active plugins in order to reduce conflicts, generating a **Merged Objects.esp** file which we will have to place at the end of our load order. This is very useful when, for example, you have a mod that modifies the stats on the Glass Armor while another modifies how it looks like: TES3Merge will merge both changes into a single plugin.

- Run TES3Merge in MO2. Once it's finished, press any key to exit.
- **Merged Objects.ESP** will now be present at the end of your load order. Make sure you activate it.

Last but not least, Merged Objects.ESP makes a handufl of unintended changes to the Imperial Netch Blade, Iron Spider Dagger, and Stormkiss records when using BTBGI Necro Edit.

- In [**TESAME**](https://github.com/Sigourn/morrowind-improved/blob/master/mwtools.md#tesame), delete the following records: 
  - Weapon **iron spider dagger**
  - Weapon **imperial netch blade**
  - Weapon **Stormkiss**
- This omits the unintended changes made by Merged Objects to these weapons.

With this, our conflict solving is over and done with.

### Running Distant Land

MGE XE's Distant Land setup should be re-run. If you followed the steps [**in this section**](https://github.com/Sigourn/morrowind-improved/blob/master/setup.md#distant-land-tab) earlier, the process will be much easier.

- Run MGE XE in MO2.
- In the **Distant Land** tab, click *Distant land generator wizard*.
- Click *Select all*, and then *Continue*.
- Click *Run above steps using saved / default settings*.
- Once the statics have been created, simply click *Finish*.

### Closing commments

Broadly speaking, these are the steps you should follow whenever you install new mods.

- Get a reliable install order and load order working.
- Synchronize mod masters.
- Clean dirty plugins.
- Solve conflicts.
- Generate Distant Land to account for mods that may modify the worldspace.

## IN-GAME CONFIGURATION

**General adjustments**

Launch Morrowind and make the following adjustments.

- Under the **Options** menu, go to the *Video* tab.
- The *Gamma Correction* slider lets you increase/decrease the brightness of your game. I like to play Morrowind with the slider roughly 40-45% of the way from left to right, making the game look less washed out.
- Turn the *Real-time Shadows* slider all the way to the left, disabling them. These shadows look pretty bad, are glitchy, and not worth the performance hit.

The following mods require additional configuration through the in-game **Mod Configuration** menu.

**abot's Smart Journal**
- Set *Add a prefix in order to group quest names?* to 0. This will remove the lag when opening the quest page without this option set to 0.
- Disable every option below *Sort quests list by quest name?*. These options are mostly useful to troubleshoot mods. 

**abot's Tooltip**
- Disable *Show item Value/Weight Ratio in tooltip*.

**Clock Block**
- Set *Clock position* to Bottom.
- Set *Clock type* to Game time.

**Continue**
- (Optional) Enable *Hide Credits Button* and *Hide New Game Button (In Game)*.

**Controlled Consumption**
- Set *Current consumption module* to Vanilla NPC Style (Necro Edit).

**Dynamic Timescale**  
Cell Settings
- Set *Wilderness timescale* to 60. This will slow down the timescale when in wilderness cells by 50%. In my opinion, the default value is way too high.

**Essential Indicators**  
General Settings
- Disable *Essential Item Indicator*.
- Disable *Essential NPC Indicator*.
- Disable *Quest-Giver NPC Indicator*.
- Disable *Quest-Giver Faction Sensibility*.

Crosshair Settings  
- Set *Crosshair Scale* to 80%.
- Set *Sneaking Crosshair Scale* to 80%.

**HardTrade**
- Disable *Limit player stats to 100 when trading*.

**Let There Be Darkness - Lua Lighting Overhaul**  
General and Cell Settings
- Set *Cell lighting value overrides* to NONE.
- If you've installed the specialprocess shader in **Setup**, set all three *Ambient color adjustments* to 75.

Light Settings  
- Disable *Use TLaD overrides for radius and color of light sources?*.

**Limited Leaping**
- Set *Cooldown between jumps* to 1.
- Set *Minimum fatigue to jump* to 20. This matches the fatigue drain for jumping when using BTB's Game Improvements.

**Putting Power in Willpower**
- Enable *Allow negative Resist Bonus*.

**Security Enhanced**
- Disable *Enable Lockpick Auto-Equip On Locked Object Activation*.
- Disable *Enable Probe Auto-Equip On Trapped Object Activation*.

**UI Expansion**  
Please bear in mind that your game *may* crash when configuring this mod. That said, whatever changes you made will persist after running the game again.

- Set *Auto-select search bar* to None. I found this option to be particularly annoying as I would accidentally press one of my movement keys after opening the menu, and suddenly one of my search bars would be filtered.
- (Optional) Set *Use verbose buttons instead of icons for inventory filtering?* to No.
- (Optional) Set *Use search bars?* to No.

**Weapon Sheathing**
Exclusions
- Click *Plugins*, and click *animated_morrowind - merged.esp*. This will move the plugin to the *Blocked* list.
  - This will avoid issues between both mods where Animated Morrowind Merged's NPCs would sometimes refuse to use items alongside their animations.

### Mod keybindings

The mods installed in this guide and configured as mentioned above will use the following keys:

- **Hot Quests**: **U** key for Quests, **I** key for Topics.
- **Kill Command**: **K** key to order attacks.
- **Security Enhanced**: **L** key to equip lockpicks, **P** key to equip probes.
- **Scriptable Scriptures**: **B** key to switch between open and closed scriptures.
- **Torch Hotkey**: **C** key to equip light sources.

## CREDITS

I want to thank the following mod authors for their original mods which have been edited for inclusion in this guide.

- Aoimevelho, for [**Cavern of the Incarnate Overhaul**](https://www.nexusmods.com/morrowind/mods/42860/), which was edited to remove all cavern edits while keeping the changes to the False Incarnates intact.
- Lucevar, for [**LDM - Choices & Consequences**](https://discord.com/channels/210394599246659585/677279423250038834), which was edited for compatibility with **Early Transport to Mournhold**.
- R-Zero, for [**Lucky Strike - A Critical Hit Mod**](https://www.nexusmods.com/morrowind/mods/45765), which was edited to fix some issues with the mod.
- NullCacade, for [**Controlled Consumption**](https://www.nexusmods.com/morrowind/mods/45624), which was edited to include ingredient consumption restrictions.
- Archimag, for [**HardTrade**](https://www.nexusmods.com/morrowind/mods/47368), which was edited to remove the investing feature and unwanted GMST changes for compatibility with other mods.
- Remiros and Half11, for [**Morrowind Anti-Cheese**](https://www.nexusmods.com/morrowind/mods/47305), which was edited for compatibility with **Ownership Overhaul**.
- BTB and Necrolesian, for [**BTB's Game Improvements - Necro Edit v2.0**](https://www.nexusmods.com/morrowind/mods/47129?), which was edited to remove Morrowind Advanced's creature stat buffs.

## COMPATIBILITY

Morrowind# is a big guide and touches on many aspects of the game. Though this guide is presented "as is", it doesn't mean you can't install other mods on top; only that you should think twice about what you are installing.

For reference, here is a list of known mods in the guide that tend to have compatibility issues with other mods.

- **Ownership Overhaul**: this mod touches on a *lot* of items in the game which are unowned, including doors, and it's not unusual at all for other mods (particularly big overhauls, like towns and cities) to override many of the changes made by this mod to a given location (e.g. a Pelagiad overhaul overriding the ownership of many items). Moreover, mods that add items to the game world may not account for ownership either, meaning those items are free for the taking.
  - Recommendation: just load conflicting .esms and .esps after Ownership Overhaul.
- **Yet Another Guard Diversity**: this mod replaces vanilla guards with unique guards selected from leveled lists. But because of how this mod works, it is perfectly possible for a mod to override its changes (by moving the vanilla guards around) and have the guards revert to their vanilla, generic appearance. This would be most noticeable with Imperial Legion guards who don't wear closed helmets (unlike their Hlaalu, Redoran, Telvanni, and Indoril counterparts). Moreover, new guards added to the game world will most likely have a generic appearance as well.
  - Recommendation: just load conflicting .esps after Yet Another Guard Diversity.
- **Morrowind Anti-Cheese**, **BTB's Game Improvements - Necro Edit**: these mods make drastic changes to the game's balance, including the addition of new enemies to vanilla locations, stat tweaks to equipment and items, and edits to NPCs' inventories, stats, and spells. Any large overhaul that affects NPCs or vanilla items will quite possibly conflict with these mods (e.g. a faction overhaul, such as Vvardenfell Brotherhood or Morag Tong Polished). Depending on the conflict, it can be virtually harmless (without looking at TES3View you wouldn't even tell there is a conflict) or serious (an NPC that should have been buffed to a considerable degree reverts back to its vanilla, puny mook state).
  - Recommendation: use TES3View to look at conflicts and determine the best course of action, whether that is modifying your load order, using TESAME to delete conflicting records, or create a patch using the Construction Set.

[<< Back to Main](https://github.com/Sigourn/morrowind-improved/blob/master/readme.md#morrowind)  
[<< Back to Setup](https://github.com/Sigourn/morrowind-improved/blob/master/setup.md#setup)
