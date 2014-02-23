Jarmodding (putting stuff in the minecraft .jar) is currently not supported, also none of the main developers feel like doing it right now, so if no one submit a pull request support won't be added for now.

Mojang have said they DO NOT want people to put things into the jar, and there exist several alternative ways of that jar mods could be installed in (used by some jar mods):
* As a MinecraftForge mod (simply drop into the mods/ folder). Requires a version of forge for the minecraft version.
* As a launchwrapper tweaker, doesn't require forge and still is a relatively clean way of installing. Also see the bottom.

### List of jarmods

| Name      | Forge | Launchwrapper |
| --------- | ----- | ------------- |
| OptiFine  | Yes   | Yes*          |
| MCPatcher | No    | No            |

TODO: Add more mods here

\* See [MultiMC and Optifine](https://github.com/MultiMC/MultiMC5/wiki/MultiMC-and-Optifine) for how to install optifine without forge, using launchwrapper

### More on launchwrapper (kinda more for modders)

Launchwrapper is a library supplied by mojang for injecting bytecode into the game in a cleaner way. Mojang use it for launching legacy instances from the new launcher. The code for the library is available [here](https://github.com/Mojang/LegacyLauncher). It is also used by MinecraftForge, LiteLoader, OptiFine and a few others for "cleanly" injecting stuff into the game. For using launchwrapper, you do not have to do anything to the minecraft jar, it's as simple as adding

    {
        "name": "net.minecraft:launchwrapper:<version>"
    }

to the libraries array, setting "mainClass" to "net.minecraft.launchwrapper.Launch" and adding "--tweakClass &lt;name of class&gt;" to the "minecraftArguments" string in the instance JSON. &lt;version&gt; depends on the version of Minecraft (try 1.7, 1.8, 1.9 for the recent versions of minecraft) and &lt;name of class&gt; should be a class implementing `net.minecraft.launchwrapper.ITweaker`. From there it's possible to pretty much do whatever you want.