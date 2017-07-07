## Minecraft not launching or crashing on launch
There are many issues possible for this, here are some issues and solutions.

#### Mods are a different version
Makes sure that all the mods for the instance you are launching are for the version of Minecraft you're launching -- eg. 1.6.4 mods for Minecraft 1.6.4, 1.7.10 mods for Minecraft 1.7.10 and so on.

#### Putting forge/LiteLoader mods in jar mods instead of loader mods
Whether you're loading forge mods or LiteLoader mods, they all need to be added via. loader mods. Jar mods are added to the Minecraft jar, and that is a rare occurrence with most recent mods.

### Insufficient memory allocated to Java
If you are trying to load a heavy instance with lots of mods, you may need to allocate more maximum memory to the instance. You can do this by:
1. Right click the instance and choose "Instance settings"
2. Under the Java tab, check the "Memory" checkbox
3. Raise the "Maximum memory allocation" to 2048MB

## Graphics issues

### Hybrid laptop graphics (optimus and similar)
If you get slow rendering and Minecraft using the integrated graphics card instead of the dedicated one, there are some ways to fix that:

#### Windows
In general, the graphics drivers look for the binary name in order to enable the dedicated GPU. Rename `MultiMC.exe` to `Minecraft.exe`.  This fools them into enabling it.

The same applies to many other situations where graphics are an issue on Windows:

Rename the .exe and it might just work better.

#### Linux
You can use the [Wrapper command option in the Java settings](https://github.com/MultiMC/MultiMC5/wiki/Java-settings#custom-commands) together with `optirun` or similar wrappers.

### OpenGL format not accelerated or graphical glitches ingame
You need to update your graphics drivers. If they are already the latest, your graphics card is too old.

- AMD: http://support.amd.com/en-us/download
- NVidia: http://www.nvidia.com/Download/index.aspx?lang=en-us
- Intel: https://downloadcenter.intel.com/

## Can't log in
Minecraft login can be blocked by several issues:

#### You changed your account name recently
In MultiMC, remove your Mojang account and add it again.

#### Network blocking or Mojang servers being down
Generally, you can detect this by looking at the status icons on the lower right of the MultiMC window. Clicking them leads to [The Mojang help page.](https://help.mojang.com/). If the auth and session servers are having issues, you just have to wait. If you can access the page, but the status icons show as offline, or if both are offline, your network access might be broken or filtered. We can't help you with that.

#### Secure access problems
If the access to the Mojang auth servers is compromised or impossible, you will get a scary error message. Please report these as bugs, along with uploading the MultiMC log file (MultiMC-0.log).

## Folders

### Copy contents of x folder
There may come a time when you have many files all over, or have an ssd and want to save as much space as possible. Instead of giving you the ablility to copy over/keep updated a second folder for you, we'll walk you through how to use features already in you OS to do so.

#### Windows
Just like Linux, you just have to type one command,

```mklink /j "c:\users\Will\Desktop\multimc\mods" c:\users\Will\.minecraft\mods```

The following command makes a linked folder or symlink from .minecraft\mods to multimc\mods

#### Linux
The linux command is a little easier,

```ln -s /home/Will/.minecraft/mods /home/Will/multimc/mods```

## Poor performance and/or lag ingame

### Solution 1: Get a better PC
_Self-explanatory_
If you want advice and suggestions on what kind of computer or computer components to get within a certain budget, ask in the #advice channel of [GadgetWorks' Discord server](https://discord.gg/Qqbddqg).

### Solution 2: Lower your settings
1. On Minecraft's main menu, click "Options"
2. Click "Video settings"
3. Lower the render distance
4. Set "Graphics" to "Fast" instead of "Fancy"
5. Set "Smooth Lighting" to "Minimum" instead of "Maximum"
6. Turn on VBOs if the option is available (will yield a large performance boost on AMD systems)

### Solution 3: Reduce un-necessary third-party background processes (Windows)
Sometimes (or often if you're click happy or a more novice user), you end up installing PUPs on your PC along with what you intended to install, which then adds bloat and causes performance regression - especially on the CPU side of things which Minecraft is most sensitive to.

Use the follow steps to help reduce the amount of third-party background processes (these instructions apply to Windows 8/8.1/10 - if you are using Windows 7, consider upgrading to a newer and more efficient OS first):
1. Press Ctrl + Alt + Del and open Task Manager
2. Go to the Startup tab in Task Manager
3. Click on "Startup impact" so that it sorts the items from highest impact to lowest impact
4. Click on a each high impact item you don't want running in the background constantly as soon as your computer turns on and click the Disable button.
5. Do the same for medium impact items.
**NOTE: Do not disable startup items by the publishers AMD, Intel, NVidia, Realtek or Microsoft as these may be required for your computer to work optimally.** 

6. Close task manager and press Win + R to open the run prompt
7. Enter `msconfig` in the run prompt (without the "") and click "OK"
8. Go to the Services tab and make sure the "Hide all Microsoft services" checkbox is checked
9. Same as with the startup items, disable any third-party background services you don't want running in the background
**WARNING: Do not disable services by the publishers AMD, Intel, NVidia, Realtek or Microsoft as these are required for your computer to work properly.** 

10. Finally, restart your computer to apply the changes. If anything goes wrong, undo your changes by following these steps backwards or contact [GadgetWorks](https://discord.gg/Qqbddqg) for free help and support.