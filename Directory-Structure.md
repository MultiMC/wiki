Not all files/directories might be available, depending on your setup

## Linux

```
<MultiMC root>
├── accounts
│   └── skins
│       └── <username>.png
├── accounts.json
├── assets
│   ├── indexes
│   │   ├── <version>.json
│   │   └── legacy.json
│   ├── objects
│   │   ├── 00
│   │   │   ├── 000<some more stuff here>
│   │   │   ├── ...
│   │   │   └── 00F<some more stuff here>
│   │   ├── ...
│   │   └── ff
│   └── virtual
│       └── legacy
├── bin
│   ├── jars
│   │   ├── JavaCheck.jar
│   │   └── NewLaunch.jar
│   ├── <libraries>
│   ├── MultiMC
│   └── updater
├── icons
├── instances
│   ├── instgroups.json
│   ├── LiteLoader 1.7.2
│   │   ├── instance.cfg
│   │   ├── minecraft
│   │   ├── patches
│   │   │   └── com.mumfrey.liteloader.json
│   │   └── version.json
│   ├── Forge 1.6.4
│   │   ├── instance.cfg
│   │   ├── minecraft
│   │   ├── patches
│   │   │   └── net.minecraftforge.json
│   │   └── version.json
│   ├── Vanilla 1.5.2
│   │   ├── instance.cfg
│   │   ├── instMods
│   │   └── minecraft
│   └── Vanilla 1.7.2
│       ├── instance.cfg
│       ├── minecraft
│       └── version.json
├── libraries
├── lwjgl
│   └── 2.9.0
│       ├── jinput.jar
│       ├── lwjgl.jar
│       ├── lwjgl_util.jar
│       └── natives
├── metacache
├── mods
│   ├── minecraftforge
│   │   ├── forge-1.6.4-9.11.1.965-installer.jar
│   │   ├── forge-1.7.2-10.12.0.999-installer.jar
│   │   ├── json
│   │   └── list.json
│   └── liteloader
│       └── versions.json
├── MultiMC
├── MultiMC-0.log
├── MultiMC-1.log
├── MultiMC-2.log
├── MultiMC-3.log
├── MultiMC-4.log
├── multimc.cfg
├── notifications.json
├── plugins
│   ├── imageformats
│   │   ├── libqgif.so
│   │   ├── libqico.so
│   │   ├── libqjpeg.so
│   │   └── libqwbmp.so
│   └── platforms
│       └── libqxcb.so
├── qt.conf
├── translations
│   └── mmc_de.qm
└── versions
    └── \<Minecraft version\>
        └── \<Minecraft version\>.jar
```

# Explanation

| File/Directory | Description |
| --- | --- |
| accounts.json | All your accounts are saved here. No passwords are saved here, though the different tokens could be used to play Minecraft as you, so be careful |
| assets/indexes/ | The files here contain information about the assets for different versions of the game, like which asset ID belongs to which asset. |
| assets/objects/ | All "new" assets are stored here. They all have a 40 letter hexadecimal ID, and are sorted into folders according to their first 2 letters. |
| assets/virtual/legacy/ | Assets for older versions of Minecraft |
| bin/jars/ | Since MultiMC isn't a Java program we use a few different Java applications for things like launching the game. Those are stored here. |
| bin/MultiMC | LINUX ONLY: This is the main executable, but it should never be called directly. Always use the script at root |
| bin/MultiMC.exe | WINDOWS ONLY: This is the main executable. |
| bin/updater | LINUX AND OSX: This is the application MultiMC uses to update itself and should not be used by itself |
| bin/updater.exe | WINDOWS ONLY: Same as above |
| bin/\<libraries\> | Files in bin/ ending in .dll (windows) or .so (others) are dependencies of MultiMC |
| icons/ | All custom icons you give to MultiMC are stored here |
| instances/instgroups.json | This file defines in which groups the instances are sorted |
| instances/\<instance\>/instance.cfg | This file keeps all the instance settings, such as memory options, as well as it's name etc. |
| instances/\<instance\>/version.json | 1.6+ ONLY: This file contains all the information needed to launch a vanilla instance, like libraries needed etc. |
| instances/\<instance\>/custom.json | 1.6+ ONLY, **DEPRECATED**: Like version.json, but for usage in modded scenarios. Can be used for completely overriding version.json, but it's recommended to use [patches](JSON Patches) instead |
| instances/\<instance\>/minecraft/ | This is the "normal" Minecraft directory, which contains, saves/, mods/ etc. |
| instances/\<instance\>/instMods/ | Pre-1.6 ONLY: The directory containing jarmods |
| libraries/ | This contains all of Minecrafts dependencies, see below for more info |
| lwjgl/ | LWJGL stuff is stored here |
| metacache | This JSON file contains information about most downloaded files and is used for keeping track of them and making sure they are always up-to-date |
| mods/minecraftforge/*.jar | Forge installers |
| mods/minecraftforge/json | Local copy of the Forge version list (gradle generation) |
| mods/minecraftforge/list.json | Local copy of the Forge version list (pre-gradle generation) |
| mods/liteloader/versions.json | Local copy of the LiteLoader version list |
| MultiMC | LINUX ONLY: Runner script, does some pre-launch checking, should be used instead of bin/MultiMC |
| MultiMC-*.log | MultiMC logs, the logs of the five last launches are kept |
| multimc.cfg | MultiMC global settings |
| notifications.json | Local copy of the notifications list |
| plugins/ | Needed by Qt |
| qt.conf | Needed by Qt |
| translations/mmc_\<lang\>.qm | Translations of MultiMC, [[Translating MultiMC]] for more info |
| versions/\<Version\>/\<Version\> | All Minecraft Jars |