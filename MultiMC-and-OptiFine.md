## Minecraft versions which have Forge

Just use OptiFine like any other Forge mod

## Minecraft versions that don't have Forge

* Make a new instance in MultiMC with the wanted version of Minecraft
* Open the instance directory
* Create a file in`patches/` called `optifine.json` and paste the following into it:
```
{
    "+libraries": [
        {
            "name": "net.minecraft:launchwrapper:1.12"
        },
        {
            "name": "optifine:OptiFine:<Version Of OptiFine>",
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
    "mcVersion": "<Version Of Minecraft>",
    "name": "OptiFine",
    "order": 200,
    "version": "<Version Of Optifine>"
}
```
* Download OptiFine and put the file into `<MMC>/libraries/optifine/OptiFine/<version of optifine>/`
* Rename the file to `OptiFine-<Version Of OptiFine>.jar`, where `<Version Of OptiFine>` is the part of the downloaded file name after the first underscore. This means OptiFine_1.7.4_HD_U_C7.jar gets renamed to OptiFine-1.7.4_HD_U_C7.jar.
* Replace `<Version Of OptiFine>` in the `optifine.json` file the OptiFine version (1.7.4_HD_U_C7 for example).
* Replace `<Version Of Minecraft>` in the file with the version of Minecraft (1.7.5 for example)
7. Launch the instance from MultiMC

### Troubleshooting and FAQ

* `java.lang.ClassDefNotFound: ...`: make sure that the path to OptiFine that's outputted on the console is actually pointing to the file you downloaded.
* This broke my game!: No warranty is given. While we might help you, when doing stuff like this you are entirely on your own.