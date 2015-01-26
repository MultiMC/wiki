### What am I doing here?

* You got sent here because you asked how to install a jar mod with MultiMC: Read the text under the first two headers.
* You are a modder and got sent here because you are modifying the Minecraft jar: Read the text under the first and the third header.

### About

Mojang have said they DO NOT want people to put things into the jar, and there exist several alternative ways of that jar mods could be installed in (used by some jar mods):
* As a MinecraftForge mod (simply drop into the mods/ folder). Requires a version of forge for the minecraft version.
* As a launchwrapper tweaker, doesn't require forge and still is a relatively clean way of installing. Also see the bottom.

If you are a user who wants to install a jar mod with MultiMC you have three options:

1. Find out if the mod can be installed in any other way (see next header)
2. Go and ask the author of the mod to fix his stuff. Give them the link to this page.
4. MultiMC does include jar mod support. However, we would like to discourage the use of those. If you have other options, please use them. If not, you can add jar mods in the [[Instance version]] page of the Edit instance dialog.

### List of jarmods

| Name      | Forge | Launchwrapper |
| --------- | ----- | ------------- |
| OptiFine  | Yes   | Yes*          |
| MCPatcher | No    | No**          |
| Minecrift | NO    | Yes***        |

TODO: Add more mods here

\* See [MultiMC and Optifine](https://github.com/MultiMC/MultiMC5/wiki/MultiMC-and-Optifine) for how to install optifine without forge, using launchwrapper

\** MCPatcher can be made working, see [here](http://www.minecraftforum.net/topic/1000645-multimc-5-windows-linux-mac/page__st__4100#entry29778001) and a few posts up

\*** [Minecrift](https://github.com/MultiMC/MultiMC5/wiki/Minecrift) is special see its wiki page for more info.

### More on launchwrapper (kinda more for modders)

Launchwrapper is a library supplied by mojang for injecting bytecode into the game in a cleaner way. Mojang use it for launching legacy instances from the new launcher. The code for the library is available [here](https://github.com/Mojang/LegacyLauncher). It is also used by MinecraftForge, LiteLoader, OptiFine and a few others for "cleanly" injecting stuff into the game. For using launchwrapper, you do not have to do anything to the minecraft jar, it's as simple as adding

    {
        "name": "net.minecraft:launchwrapper:<version>"
    }

 at the top of the libraries array, setting "mainClass" to "net.minecraft.launchwrapper.Launch" and adding "--tweakClass &lt;name of class&gt;" to the "minecraftArguments" string in the instance JSON (custom.json in MultiMC). &lt;version&gt; depends on the version of Minecraft (try 1.7, 1.8, 1.9 for the recent versions of minecraft) and &lt;name of class&gt; should be a class implementing `net.minecraft.launchwrapper.ITweaker`. Add another library entry above the launchwrapper one:

    {
        "name": "<part1>:<part2>:<version>",
        "MMC-hint": "local"
    }

Then place the jar file with the ITweaker class and the rest of the mod in `libraries/<part1>/<part2>/<version>/<part2>-<version>.jar`. For the Mojang Launcher you can omit the MMC-hint field.

When using MultiMC you can even be really fancy and add either a "url" (`<url>/<part1>/<part2>/<version>/<part2>-<version>.jar`) or a "MMC-absoluteUrl" field, MultiMC will then download the mod from that URL. Remember to omit the MMC-hint field if you want this to happen though.

There isn't a lot of a difference between how MultiMC and how the Mojang Launcher handle this stuff, so this applies to both launchers.