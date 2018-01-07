## Minecraft versions which have Forge

Just use OptiFine like any other Forge mod

## Minecraft versions that don't have Forge

* Make a new instance in MultiMC with the wanted version of Minecraft.
* Click `Edit Instance` - it should open the `Version` page of the instance.
* Click `Add Empty`.
* Set `uid` to `optifine.OptiFine` and name to `OptiFine`.
* Select the newly created component and click `Edit` - this should open the file in a text editor.
* Edit the JSON to look like one of the examples, then save the file.
* Download OptiFine and save the jar file in `<Instance>/libraries/`
* Launch the instance from MultiMC

If the example doesn't fit the OptiFine version exactly, you may have to change the versions in the file. For example replace all occurences of `1.7.10_HD_U_E3` with `1.7.10_HD_U_F1`.

You can use the version page to check the file for errors - obvious mistakes will show up in the `Version` page as soon as you click the `Refresh` button.

If the JSON file doesn't open in a text editor, make sure your operating system is set up to open `.json` files in one first.

### Examples

#### Minecraft 1.7.10
```
{
    "formatVersion": 1,
    "+libraries": [
        {
            "name": "net.minecraft:launchwrapper:1.12"
        },
        {
            "name": "optifine:OptiFine:1.7.10_HD_U_E3",
            "MMC-hint": "local",
            "MMC-filename": "OptiFine_1.7.10_HD_U_E3.jar"
        }
    ],
    "+tweakers": [ "optifine.OptiFineTweaker" ],
    "fileId": "optifine.OptiFine",
    "mainClass": "net.minecraft.launchwrapper.Launch",
    "requires": [
        {
            "uid": "net.minecraft",
            "equals": "1.7.10"
        }
    ],
    "name": "OptiFine",
    "version": "1.7.10_HD_U_E3"
}
```

### Troubleshooting and FAQ

* `java.lang.ClassDefNotFound: ...`: make sure that the path to OptiFine that's outputted on the console is actually pointing to the file you downloaded.
* This broke my game!: You can always remove the patch and it's as if it was never there...