# Frequently Asked Questions

## Minecraft not launching or crashing on launch
There are many issues possible with this, here are some issues and solutions.

### Not the right Java version
This is a very frequently addressed problem. Please read this dedicated wiki article [[Using the right Java]] to setup the correct Java version. 

### Mods are a different version
Makes sure that all the mods for the instance you are launching are for the version of Minecraft you're launching -- eg. 1.6.4 mods for Minecraft 1.6.4, 1.7.10 mods for Minecraft 1.7.10 and so on.

### Putting forge/LiteLoader mods in jar mods instead of loader mods
Whether you're loading forge mods or LiteLoader mods, they all need to be added via. loader mods. Jar mods are added to the Minecraft jar, and that is a rare occurrence with most recent mods.

### Insufficient memory allocated to Java
If you are trying to load a heavy instance with lots of mods, you may need to allocate more maximum memory to the instance. You can do this by:
1. Right-click the instance and choose "Instance settings"
2. Under the Java tab, check the "Memory" checkbox
3. Raise the "Maximum memory allocation" to 2048MB

More details here: [[Increasing Java's memory allocation]]

If your issue is still not resolved you can ask for help in [MultiMC](https://discord.gg/rzK54qN) discord server.

## Graphics issues

### Hybrid laptop graphics (Optimus and similar)
If you get slow rendering and Minecraft using the integrated graphics card instead of the dedicated one, there are some ways to fix that:

#### Windows
In general, the graphics drivers look for the binary name in order to enable the dedicated GPU. Rename `MultiMC.exe` to `Minecraft.exe`.  This fools them into enabling it.

The same applies to many other situations where graphics are an issue on Windows:

Rename the .exe and it might just work better.

#### Linux
You can use the [Wrapper command option in the Java settings](https://github.com/MultiMC/MultiMC5/wiki/Java-settings#custom-commands) together with `optirun` or similar wrappers.

### OpenGL format not accelerated or graphical glitches in-game
You need to update your graphics drivers. If they are already the latest and you are using an Intel GPU read [[Unsupported Intel GPUs]]

- AMD: http://support.amd.com/en-us/download
- NVidia: http://www.nvidia.com/Download/index.aspx?lang=en-us
- Intel: https://downloadcenter.intel.com/

## Can't log in
Minecraft login can be blocked by several issues:

### Network blocking or Mojang servers being down
You can first check the [Mojang Status Twitter](https://twitter.com/MojangStatus), if the auth and session servers are having issues, you just have to wait. When there's no known issues, your network access might be broken or filtered. You can join us on [Discord](https://discord.gg/rzK54qN) to help you troubleshoot.

### Secure access problems
If the access to the Mojang auth servers is compromised or impossible, you will get a scary error message. Please report these as bugs, along with uploading the MultiMC log file (MultiMC-0.log).

## Poor performance and/or lag in game

### Solution 1: Get a better PC
_Self-explanatory_

### Solution 2: Lower your settings
1. On Minecraft's main menu, click "Options"
2. Click "Video settings"
3. Lower the render distance
4. Set "Graphics" to "Fast" instead of "Fancy"
5. Set "Smooth Lighting" to "Minimum" instead of "Maximum"
6. Turn on VBOs if the option is available (will yield a large performance boost on AMD systems)
7. Set Mipmap Levels to 0

### Solution 3: Reduce un-necessary third-party background processes (Windows)
Sometimes (or often if you click happy or a more novice user), you end up installing PUPs on your PC along with what you intended to install, which then adds bloat and causes performance regression - especially on the CPU side of things which Minecraft is most sensitive to.

Use the following steps to help reduce the number of third-party background processes (these instructions apply to Windows 8/8.1/10 - if you are using Windows 7, consider upgrading to a newer and more efficient OS first):
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

10. Finally, restart your computer to apply the changes. If anything goes wrong, undo your changes by following these steps backwards or join us on [Discord](https://discord.gg/rzK54qN) for further support.
