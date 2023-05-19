Welcome to ModEngine! ModEngine is a DLL injection library for Souls games/Sekiro that adds new features
for modders and the users of mods.

Some current features include:
* Blocking network access while using mods to prevent banning
* Using an alternate save file for mods so that it won't cause banning and mods won't interfere with vanilla save
* File overrides allow loading of mods with changed files in a dedicated directory, even without UXM unpacking
* Loading override files with fallback to files from the game archives-this means no UXM required for mod users
* Patching to allow loading of loose parambnd files instead of encrypted regulation (data0) file

Installation is simple: simply place the dinput8.dll and modengine.ini files in the Sekiro
directory (same directory sekiro.exe is located). This will typically be located at
C:\Program Files (x86)\Steam\steamapps\common\Sekiro unless you have steam install somewhere else.
To uninstall, all you need to do is either delete or rename (to anything) dinput8.dll.

Usage for modders:
Choose a directory name for your mod. It defaults to \mod but it's recommended you choose something more unique for
your mod. Edit the override directory in modengine.ini to your new directory (\ is required). Decide all the features
you need and enable them in modengine.ini. If you expanded your archives with UXM but didn't apply the UXM patch, you can
enable an option to get the same functionality. You can place your override files inside the same directory the file would
be in the root directory but inside the mod directory instead. For example, if your mod directory is \mods, and you modify
map\mapstudio\m30_00_00_00.msb.dcx, you can place the modified version at \mods\map\map\mapstudio\m30_00_00_00.msb.dcx and the
game with mod engine will load it instead of the base file or the archived file. This means you can simply distribute \mod with
your modified files and mod engine (with UXM file loading disabled) to end users, and UXM won't be needed. You can also use it
for development and not modify your base unpacked files at all.

Copyright and credits:
ModEngine code is (C) 2020 Katalash. All rights reserved.
Special thanks to Pav for ASM patch for loose parambnd files.

You are free to distribute and UNMODIFIED ModEngine WITH a mod with the purpose of ModEngine being to help enable the mod.
ModEngine dinput8.dll should not be modified without permission, but modengine.ini can (and should) be modified.