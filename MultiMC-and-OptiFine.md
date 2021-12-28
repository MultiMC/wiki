## Minecraft versions which have Fabric (after and including 1.14)

Install Fabric, then add Optifine along with https://www.curseforge.com/minecraft/mc-mods/optifabric as mods.

## Minecraft versions which have Forge (before 1.13)

Just use OptiFine like any other Forge mod.

## Minecraft versions that don't have Forge or Fabric

### The jar mod way (any version)

* Make a new instance in MultiMC with the wanted version of Minecraft.
* Install the same version in the Mojang launcher
* Run the desired version of Optifine as an installer and make it extract the jar
* Add the extracted jar on the Version page of the instance (Add to Minecraft.jar)

### The launchwrapper tweaker way (listed versions)

* Make a new instance in MultiMC with the wanted version of Minecraft.
* Click `Edit Instance` - it should open the `Version` page of the instance.
* Click `Add Empty`.
* Set uid to `optifine.OptiFine` and name to `OptiFine`.
* Select the newly created component and click `Edit` - this should open the file in a text editor.
* Edit the JSON to look like one of the examples, then save the file.
* Download OptiFine and save the jar file in `<Instance>/libraries/`. Create the `libraries` folder if it doesn't exist.

  If you look at the whole path, it should be something like this:
  ```
  .../MultiMC/instances/<Instance>/libraries/OptiFine_1.13_HD_U_E3_beta4.jar
  ```

* Launch the instance from MultiMC

If the example doesn't fit the OptiFine version exactly, change the version. For example replace all occurences of `1.7.10_HD_U_E3` with `1.7.10_HD_U_F1`.

You can use the version page to check the file for errors - obvious mistakes will show up in the `Version` page as soon as you click the `Refresh` button.

If the JSON file doesn't open in a text editor, make sure your operating system is set up to open `.json` files in one first.

#### Examples

##### Minecraft 1.18.1 with OptiFine 1.18.1_HD_U_H4
```
{
    "formatVersion": 1,
    "name": "OptiFine",
    "+libraries": [
        {
            "name": "net.minecraft:launchwrapper:of-2.3",
            "url": "https://files.multimc.org/maven/"
        },
        {
            "name": "optifine:OptiFine:1.18.1_HD_U_H4",
            "MMC-hint": "local",
            "MMC-filename": "OptiFine_1.18.1_HD_U_H4.jar"
        }
    ],
    "+tweakers": [ "optifine.OptiFineTweaker" ],
    "mainClass": "net.minecraft.launchwrapper.Launch",
    "requires": [
        {
            "uid": "net.minecraft",
            "equals": "1.18"
        }
    ],
    "uid": "optifine.OptiFine",
    "version": "1.18.1_HD_U_H4"
}
```


##### Minecraft 1.18 with OptiFine 1.18_HD_U_H3
```
{
    "formatVersion": 1,
    "name": "OptiFine",
    "+libraries": [
        {
            "name": "net.minecraft:launchwrapper:of-2.3",
            "url": "https://files.multimc.org/maven/"
        },
        {
            "name": "optifine:OptiFine:1.18_HD_U_H3",
            "MMC-hint": "local",
            "MMC-filename": "OptiFine_1.18_HD_U_H3.jar"
        }
    ],
    "+tweakers": [ "optifine.OptiFineTweaker" ],
    "mainClass": "net.minecraft.launchwrapper.Launch",
    "requires": [
        {
            "uid": "net.minecraft",
            "equals": "1.18"
        }
    ],
    "uid": "optifine.OptiFine",
    "version": "1.18_HD_U_H3"
}
```

##### Minecraft 1.13.2 with OptiFine 1.13.2_HD_U_E4
```
{
    "formatVersion": 1,
    "+libraries": [
        {
            "name": "net.minecraft:launchwrapper:1.12"
        },
        {
            "name": "optifine:OptiFine:1.13.2_HD_U_E4",
            "MMC-hint": "local",
            "MMC-filename": "OptiFine_1.13.2_HD_U_E4.jar"
        }
    ],
    "+tweakers": [ "optifine.OptiFineTweaker" ],
    "fileId": "optifine.OptiFine",
    "mainClass": "net.minecraft.launchwrapper.Launch",
    "requires": [
        {
            "uid": "net.minecraft",
            "equals": "1.13.2"
        }
    ],
    "name": "OptiFine",
    "version": "1.13.2_HD_U_E4"
}
```

##### Minecraft 1.13.1 with OptiFine 1.13.1_HD_U_E4
```
{
    "formatVersion": 1,
    "+libraries": [
        {
            "name": "net.minecraft:launchwrapper:1.12"
        },
        {
            "name": "optifine:OptiFine:1.13.1_HD_U_E4",
            "MMC-hint": "local",
            "MMC-filename": "OptiFine_1.13.1_HD_U_E4.jar"
        }
    ],
    "+tweakers": [ "optifine.OptiFineTweaker" ],
    "fileId": "optifine.OptiFine",
    "mainClass": "net.minecraft.launchwrapper.Launch",
    "requires": [
        {
            "uid": "net.minecraft",
            "equals": "1.13.1"
        }
    ],
    "name": "OptiFine",
    "version": "1.13.1_HD_U_E4"
}
```

##### Minecraft 1.13 with OptiFine 1.13_HD_U_E4
```
{
    "formatVersion": 1,
    "+libraries": [
        {
            "name": "net.minecraft:launchwrapper:1.12"
        },
        {
            "name": "optifine:OptiFine:1.13_HD_U_E4",
            "MMC-hint": "local",
            "MMC-filename": "OptiFine_1.13_HD_U_E4.jar"
        }
    ],
    "+tweakers": [ "optifine.OptiFineTweaker" ],
    "fileId": "optifine.OptiFine",
    "mainClass": "net.minecraft.launchwrapper.Launch",
    "requires": [
        {
            "uid": "net.minecraft",
            "equals": "1.13"
        }
    ],
    "name": "OptiFine",
    "version": "1.13_HD_U_E4"
}
```

##### Minecraft 1.12.2
```
{
    "formatVersion": 1,
    "+libraries": [
        {
            "name": "net.minecraft:launchwrapper:1.12"
        },
        {
            "name": "optifine:OptiFine:1.12.2_HD_U_E2",
            "MMC-hint": "local",
            "MMC-filename": "OptiFine_1.12.2_HD_U_E2.jar"
        }
    ],
    "+tweakers": [ "optifine.OptiFineTweaker" ],
    "fileId": "optifine.OptiFine",
    "mainClass": "net.minecraft.launchwrapper.Launch",
    "requires": [
        {
            "uid": "net.minecraft",
            "equals": "1.12.2"
        }
    ],
    "name": "OptiFine",
    "version": "1.12.2_HD_U_E2"
}
```

##### Minecraft 1.12.1
```
{
    "formatVersion": 1,
    "+libraries": [
        {
            "name": "net.minecraft:launchwrapper:1.12"
        },
        {
            "name": "optifine:OptiFine:1.12.1_HD_U_C7",
            "MMC-hint": "local",
            "MMC-filename": "OptiFine_1.12.1_HD_U_C7.jar"
        }
    ],
    "+tweakers": [ "optifine.OptiFineTweaker" ],
    "fileId": "optifine.OptiFine",
    "mainClass": "net.minecraft.launchwrapper.Launch",
    "requires": [
        {
            "uid": "net.minecraft",
            "equals": "1.12.1"
        }
    ],
    "name": "OptiFine",
    "version": "1.12.1_HD_U_C7"
}
```

##### Minecraft 1.12
```
{
    "formatVersion": 1,
    "+libraries": [
        {
            "name": "net.minecraft:launchwrapper:1.12"
        },
        {
            "name": "optifine:OptiFine:1.12_HD_U_C7",
            "MMC-hint": "local",
            "MMC-filename": "OptiFine_1.12_HD_U_C7.jar"
        }
    ],
    "+tweakers": [ "optifine.OptiFineTweaker" ],
    "fileId": "optifine.OptiFine",
    "mainClass": "net.minecraft.launchwrapper.Launch",
    "requires": [
        {
            "uid": "net.minecraft",
            "equals": "1.12"
        }
    ],
    "name": "OptiFine",
    "version": "1.12_HD_U_C7"
}
```

##### Minecraft 1.11.2
```
{
    "formatVersion": 1,
    "+libraries": [
        {
            "name": "net.minecraft:launchwrapper:1.12"
        },
        {
            "name": "optifine:OptiFine:1.11.2_HD_U_C7",
            "MMC-hint": "local",
            "MMC-filename": "OptiFine_1.11.2_HD_U_C7.jar"
        }
    ],
    "+tweakers": [ "optifine.OptiFineTweaker" ],
    "fileId": "optifine.OptiFine",
    "mainClass": "net.minecraft.launchwrapper.Launch",
    "requires": [
        {
            "uid": "net.minecraft",
            "equals": "1.11.2"
        }
    ],
    "name": "OptiFine",
    "version": "1.11.2_HD_U_C7"
}
```

##### Minecraft 1.11
```
{
    "formatVersion": 1,
    "+libraries": [
        {
            "name": "net.minecraft:launchwrapper:1.12"
        },
        {
            "name": "optifine:OptiFine:1.11_HD_U_C7",
            "MMC-hint": "local",
            "MMC-filename": "OptiFine_1.11_HD_U_C7.jar"
        }
    ],
    "+tweakers": [ "optifine.OptiFineTweaker" ],
    "fileId": "optifine.OptiFine",
    "mainClass": "net.minecraft.launchwrapper.Launch",
    "requires": [
        {
            "uid": "net.minecraft",
            "equals": "1.11"
        }
    ],
    "name": "OptiFine",
    "version": "1.11_HD_U_C7"
}
```

##### Minecraft 1.10.2
```
{
    "formatVersion": 1,
    "+libraries": [
        {
            "name": "net.minecraft:launchwrapper:1.12"
        },
        {
            "name": "optifine:OptiFine:1.10.2_HD_U_E7",
            "MMC-hint": "local",
            "MMC-filename": "OptiFine_1.10.2_HD_U_E7.jar"
        }
    ],
    "+tweakers": [ "optifine.OptiFineTweaker" ],
    "fileId": "optifine.OptiFine",
    "mainClass": "net.minecraft.launchwrapper.Launch",
    "requires": [
        {
            "uid": "net.minecraft",
            "equals": "1.10.2"
        }
    ],
    "name": "OptiFine",
    "version": "1.10.2_HD_U_E7"
}
```

##### Minecraft 1.10
```
{
    "formatVersion": 1,
    "+libraries": [
        {
            "name": "net.minecraft:launchwrapper:1.12"
        },
        {
            "name": "optifine:OptiFine:1.10_HD_U_E7",
            "MMC-hint": "local",
            "MMC-filename": "OptiFine_1.10_HD_U_E7.jar"
        }
    ],
    "+tweakers": [ "optifine.OptiFineTweaker" ],
    "fileId": "optifine.OptiFine",
    "mainClass": "net.minecraft.launchwrapper.Launch",
    "requires": [
        {
            "uid": "net.minecraft",
            "equals": "1.10"
        }
    ],
    "name": "OptiFine",
    "version": "1.10_HD_U_E7"
}
```

##### Minecraft 1.9.4
```
{
    "formatVersion": 1,
    "+libraries": [
        {
            "name": "net.minecraft:launchwrapper:1.12"
        },
        {
            "name": "optifine:OptiFine:1.9.4_HD_U_E7",
            "MMC-hint": "local",
            "MMC-filename": "OptiFine_1.9.4_HD_U_E7.jar"
        }
    ],
    "+tweakers": [ "optifine.OptiFineTweaker" ],
    "fileId": "optifine.OptiFine",
    "mainClass": "net.minecraft.launchwrapper.Launch",
    "requires": [
        {
            "uid": "net.minecraft",
            "equals": "1.9.4"
        }
    ],
    "name": "OptiFine",
    "version": "1.9.4_HD_U_E7"
}
```

##### Minecraft 1.9.2
```
{
    "formatVersion": 1,
    "+libraries": [
        {
            "name": "net.minecraft:launchwrapper:1.12"
        },
        {
            "name": "optifine:OptiFine:1.9.2_HD_U_E3",
            "MMC-hint": "local",
            "MMC-filename": "OptiFine_1.9.2_HD_U_E3.jar"
        }
    ],
    "+tweakers": [ "optifine.OptiFineTweaker" ],
    "fileId": "optifine.OptiFine",
    "mainClass": "net.minecraft.launchwrapper.Launch",
    "requires": [
        {
            "uid": "net.minecraft",
            "equals": "1.9.2"
        }
    ],
    "name": "OptiFine",
    "version": "1.9.2_HD_U_E3"
}
```

##### Minecraft 1.9
```
{
    "formatVersion": 1,
    "+libraries": [
        {
            "name": "net.minecraft:launchwrapper:1.12"
        },
        {
            "name": "optifine:OptiFine:1.9.0_HD_U_E7",
            "MMC-hint": "local",
            "MMC-filename": "OptiFine_1.9.0_HD_U_E7.jar"
        }
    ],
    "+tweakers": [ "optifine.OptiFineTweaker" ],
    "fileId": "optifine.OptiFine",
    "mainClass": "net.minecraft.launchwrapper.Launch",
    "requires": [
        {
            "uid": "net.minecraft",
            "equals": "1.9"
        }
    ],
    "name": "OptiFine",
    "version": "1.9.0_HD_U_E7"
}
```

##### Minecraft 1.8.9
```
{
    "formatVersion": 1,
    "+libraries": [
        {
            "name": "net.minecraft:launchwrapper:1.12"
        },
        {
            "name": "optifine:OptiFine:1.8.9_HD_U_I3",
            "MMC-hint": "local",
            "MMC-filename": "OptiFine_1.8.9_HD_U_I3.jar"
        }
    ],
    "+tweakers": [ "optifine.OptiFineTweaker" ],
    "fileId": "optifine.OptiFine",
    "mainClass": "net.minecraft.launchwrapper.Launch",
    "requires": [
        {
            "uid": "net.minecraft",
            "equals": "1.8.9"
        }
    ],
    "name": "OptiFine",
    "version": "1.8.9_HD_U_I3"
}
```

##### Minecraft 1.8.8
This one is currently broken. The 1.8.8 download is 1.8.9 and it fails to load. 

##### Minecraft 1.8
```
{
    "formatVersion": 1,
    "+libraries": [
        {
            "name": "net.minecraft:launchwrapper:1.12"
        },
        {
            "name": "optifine:OptiFine:1.8.0_HD_U_I3",
            "MMC-hint": "local",
            "MMC-filename": "OptiFine_1.8.0_HD_U_I3.jar"
        }
    ],
    "+tweakers": [ "optifine.OptiFineTweaker" ],
    "fileId": "optifine.OptiFine",
    "mainClass": "net.minecraft.launchwrapper.Launch",
    "requires": [
        {
            "uid": "net.minecraft",
            "equals": "1.8"
        }
    ],
    "name": "OptiFine",
    "version": "1.8.0_HD_U_I3"
}
```

##### Minecraft 1.7.10
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

##### Minecraft 1.7.2
```
{
    "formatVersion": 1,
    "+libraries": [
        {
            "name": "net.minecraft:launchwrapper:1.12"
        },
        {
            "name": "optifine:OptiFine:1.7.2_HD_U_F3",
            "MMC-hint": "local",
            "MMC-filename": "OptiFine_1.7.2_HD_U_F3.jar"
        }
    ],
    "+tweakers": [ "optifine.OptiFineTweaker" ],
    "fileId": "optifine.OptiFine",
    "mainClass": "net.minecraft.launchwrapper.Launch",
    "requires": [
        {
            "uid": "net.minecraft",
            "equals": "1.7.2"
        }
    ],
    "name": "OptiFine",
    "version": "1.7.2_HD_U_F3"
}
```

#### Troubleshooting and FAQ

* `java.lang.ClassDefNotFound: ...`: make sure that the path to OptiFine that's outputted on the console is actually pointing to the file you downloaded.
* This broke my game!: You can always remove the patch and it's as if it was never there...
