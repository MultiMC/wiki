## Minecraft versions which have Forge

Just use OptiFine like any other Forge mod

## Minecraft versions that don't have Forge

* Make a new instance in MultiMC with the wanted version of Minecraft.
* Open the instance folder
* If there isn't a `patches` folder, create one.
* Open the `patches` folder.
* Create a file called `optifine.json` in there, open it in a text editor and paste the following into it:
```
{
    "+libraries": [
        {
            "name": "net.minecraft:launchwrapper:1.12"
        },
        {
            "name": "optifine:OptiFine:1.9.2_HD_U_B1",
            "MMC-hint": "local"
        },
        {
            "name": "org.multimc.hacks:OptiFineHack:1",
            "MMC-absoluteUrl": "http://files.multimc.org/downloads/OptiFineHack-1.jar"
        }
    ],
    "+tweakers": [ "org.multimc.hacks.OptiFineHackTweaker" ],
    "fileId": "optifine.OptiFine",
    "mainClass": "net.minecraft.launchwrapper.Launch",
    "mcVersion": "1.9.2",
    "name": "OptiFine",
    "order": 200,
    "version": "1.9.2_HD_U_B1"
}
```
* If you use a different version of Optifine, replace the `1.9.2_HD_U_B1` with your version.
* If you use a different version of Minecraft, replace the `1.9.2` with your version.
* Save the file and close the text editor (from now on, you can open the file from MultiMC in the instance's `version` tab)
* Download OptiFine and save the jar file as `<Instance>/libraries/OptiFine-1.9.2_HD_U_B1.jar` - compared to the original file, you have to replace the first underscore with a dash and obviously replace the version to match yours.
7. Launch the instance from MultiMC

### Example for Minecraft 1.10.2 (extra hack jar is no longer necessary)

See:
https://gist.github.com/peterix/5c8b655ffafb866ccb2519f421dab671

### Troubleshooting and FAQ

* `java.lang.ClassDefNotFound: ...`: make sure that the path to OptiFine that's outputted on the console is actually pointing to the file you downloaded.
* This broke my game!: Next time, experiment on a copy of an instance. If you can't fix the instance from MultiMC, you can always remove the patch by deleting the json file.