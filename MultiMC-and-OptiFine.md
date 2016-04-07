## Minecraft versions which have Forge

Just use OptiFine like any other Forge mod

## Minecraft versions that don't have Forge

0. Make a new instance in MultiMC with the wanted version of Minecraft
1. Open the instance directory
2. If there is a file called `custom.json` delete it
3. Create a file in`patches/` called `optifine.json` and paste the following into it:
```
{
    "+libraries": [
        {
            "insert": "prepend",
            "name": "net.minecraft:launchwrapper:1.12"
        },
        {
            "MMC-hint": "local",
            "name": "optifine:OptiFine:<Version Of OptiFine>"
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
4. Download OptiFine and put the file into `<MMC>/libraries/optifine/OptiFine/<version of optifine>/`
5. Rename the file to `OptiFine-<Version Of OptiFine>.jar`, where `<Version Of OptiFine>` is the part of the downloaded file name after the first underscore. This means OptiFine_1.7.4_HD_U_C7.jar gets renamed to OptiFine-1.7.4.jar. Also replace `<Version Of OptiFine>` in the file in #3 with EXACTLY the same version.
6. Also replace `<Version Of Minecraft>` in the file in #3 with the name of the version of Minecraft (1.7.5 for example)
7. Launch the instance from MultiMC

### Troubleshooting and FAQ

* `java.lang.ClassDefNotFound: ...`: make sure that the path to OptiFine that's outputted on the console is actually pointing to the file you downloaded.
* This broke my game!: No warranty is given. While we might help you, when doing stuff like this you are entirely on your own.