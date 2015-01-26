Instructions for 1.8.1
======================

1. Create 'jarmods' and 'patches' folders in your instance directory.
2. Use the installer with the vanilla launcher
3. Copy libraries/com/mtbs3d/minecrift/1.8.1-PRE2/minecrift-1.8.1-PRE2.jar **FROM THE VANILLA LAUNCHER (.minecraft)** into the MultiMC instance's jarmods folder
4. Download optifine 1.8.1 HD Ultra B2 and save it as MultiMC/libraries/optifine/OptiFine/1.8.1_HD_U_B2/OptiFine-1.8.1_HD_U_B2.jar
5. Copy the below file into patches with the given name
6. Restart MultiMC
7. Hopefully profit

com.mtbs3d.minecrift.json
```json
{
    "+jarMods": [
        {
            "name": "minecrift-1.8.1-PRE2.jar"
        }
    ],
    "+libraries": [
        {
            "insert": "prepend",
            "name": "net.minecraft:launchwrapper:1.9"
        },
        {
            "insert": "prepend",
            "name": "org.ow2.asm:asm-all:4.1"
        },
        {
            "insert": "prepend",
            "name": "optifine:OptiFine:1.8.1_HD_U_B2",
            "MMC-hint": "local"
        },
        {
            "insert": "append",
            "name": "de.fruitfly.ovr:JRift:0.4.4.0",
            "url": "http://repo.minecraft-vr.com/"
        },
        {
            "insert": "append",
            "name": "net.aib42.mumblelink:JMumble:1.0",
            "url": "http://repo.minecraft-vr.com/"
        },
        {
            "insert": "append",
            "name": "org.json:json:20140107",
            "url": "http://central.maven.org/maven2/"
        },
        {
            "insert": "append",
            "name": "de.fruitfly.ovr:JRiftLibrary:0.4.4.0",
            "natives": {
                "windows": "natives-windows",
                "osx": "natives-osx",
                "linux": "natives-linux"
            },
            "extract": {
                "exclude": [
                    "META-INF/"
                ]
            },
            "url": "http://repo.minecraft-vr.com/"
        },
        {
            "insert": "append",
            "name": "net.aib42.mumblelink:JMumbleLibrary:1.1",
            "natives": {
                "windows": "natives-windows",
                "osx": "natives-osx",
                "linux": "natives-linux"
            },
            "extract": {
                "exclude": [
                    "META-INF/"
                ]
            },
            "url": "http://repo.minecraft-vr.com/"
        }
    ],
    "+tweakers": [
        "optifine.OptiFineTweaker"
    ],
    "fileId": "com.mtbs3d.minecrift",
    "mainClass": "net.minecraft.launchwrapper.Launch",
    "mcVersion": "1.8.1",
    "name": "Minecrift",
    "order": 10,
    "version": "1.8.1-PRE2"
}
```