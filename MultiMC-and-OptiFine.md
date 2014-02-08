## Minecraft versions which have Forge

Just use OptiFine like any other Forge mod

## Minecraft versions that don't have Forge

0. Make a new instance in MultiMC with the wanted version of Minecraft
1. Go into the instance directory
2. Make a copy of version.json called custom.json
3. Open custom.json
4. Add " --tweakClass optifine.OptiFineTweaker" after "--userType ${user_type}"
5. Add `{ "name": "net.minecraft:launchwrapper:1.7" },` at the top of the libraries array
6. Download OptiFine and put the file into <MMC>/libraries/optifine/OptiFine/
7. Rename the file to OptiFine-\<OptiFineVersion\>.jar, where \<OptiFineVersion\> is the part of the downloaded file name after the first underscore. This means OptiFine_1.7.4_HD_U_C7.jar gets renamed to OptiFine-1.7.4_HD_U_C7.jar
8. Add `{ "name": "optifine:OptiFine:<OptiFineVersion>", "MMC-hint": "local" },` at the top of the libraries array, where <OptiFineVersion> is the same as in step #7
9. Launch the instance from MultiMC
