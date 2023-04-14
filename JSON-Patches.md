# Patches 
MultiMC uses patch files to assemble the final game version. Normally, there is a Minecraft version, a LWJGL version (which Minecraft depends on) and possibly LiteLoader and Forge. Others might also exist ([[Optifine|MultiMC and OptiFine]], ...).

Patches are stored in `<instance>/patches/<name>.json`, where `<name>` should be a Java package-style descriptor, for example `net.minecraftforge` or `com.mumfrey.liteloader`.

Patches need to be referenced from the `mmc-pack.json` file.

The easiest way to add a patch is to use the MultiMC UI (add empty patch from the `Versions` page). Example of that is on the [[MultiMC and OptiFine]] page.

> **DISCLAIMER**: All of this is internal details and may be subject to unexpected changes. MultiMC will be backwards compatible with the files it made or files made based on explicit instructions ([[Optifine|MultiMC and OptiFine]] again). 
>
> However, anything abusing the knowledge of these internals and expecting them to always remain the same **WILL LIKELY BREAK** in the future. If you want to build on top of this, contact us on Discord or IRC.

## Format

The format of patches are similar to that of the vanilla version files, but with significant changes and/or additions. The formats are not directly compatible and translating between them may not be possible due to the different feature sets of both launchers.

> **DISCLAIMER**: This is by no means exhaustive, and MultiMC supports more fields and more features related to JSON version patches. This page needs updating.

Let's start with the LiteLoader patch as an example:

```json
{
  "+tweakers": [
    "com.mumfrey.liteloader.launch.LiteLoaderTweaker"
  ],
  "formatVersion": 1,
  "libraries": [
    {
      "name": "net.minecraft:launchwrapper:1.9"
    },
    {
      "name": "org.ow2.asm:asm-all:4.1"
    },
    {
      "name": "com.mumfrey:liteloader:1.7.2_05",
      "url": "http://dl.liteloader.com/versions/"
    }
  ],
  "mainClass": "net.minecraft.launchwrapper.Launch",
  "name": "LiteLoader",
  "order": 10,
  "releaseTime": "2014-07-14T20:23:26",
  "requires": [
    {
      "equals": "1.7.2",
      "uid": "net.minecraft"
    }
  ],
  "type": "release",
  "uid": "com.mumfrey.liteloader",
  "version": "1.7.2_05"
}
```
### Package metadata fields

These fields describe the package and its dependencies.

| Field | Description |
| --- | --- |
| uid | Should be the same as the `<name>` of the file. |
| name | A human-readable name of the software this describes. |
| version | The version of this patch, or the the library it is for |
| requires | List of dependencies of this patch. In this case, it depends on version 1.7.2 of Minecraft. | 
| order | DEPRECATED: Used to help sorting patches, lower number means applied earlier. |
| type | Type of the package release (release, snapshot, etc.) |
| releaseTime | Package release timestamp (ISO format). Used for sorting versions in lists. |

### Game metadata fields

These fields actually affect the launching of the game. Some can be added to or removed from using `+` or `-` before the field name, while others can only be overwritten. No + or - means overwrite.

| Field | Description |
| --- | --- |
| mainClass | This is the name of the Java class that will be used for starting the game. |
| +tweakers | WITH LAUNCHWRAPPER ONLY: A list of tweakers passed to Minecraft with `--tweakClass` |
| +traits   | A list of unique flags MultiMC will use when launching. |
| libraries | A list of libraries (artifacts) used by the game. See below for more info |

### traits

The `traits` list contains a list of any of these values.

`legacyFML`: This trait skips downloading FML libraries, used for legacy FML versions.
`legacyLaunch` and `alphaLaunch`: These traits will try to use the legacy launch using the applet wrapper.
`noapplet`: If `legacyLaunch` or `alphaLaunch` are enabled, this trait will not launch the game using the applet wrapper.
`FirstThreadOnMacOS`: This trait will add `-XstartOnFirstThread` to the JVM arguments for MacOS.
`no-texturepacks`: This trait is used to indicate texture packs should not be used.
`texturepacks`: This trait is used to indicate texture packs are being used.

### libraries

The `libraries` list contains a list of objects with the following possible fields.

`name` is the only field that is required

#### name

The 'augmented maven coordinate' of the library.

The format is `<group>:<name>:<version>[:classifier][@extension]`.
The `classifier` and `extension` parts are optional, classifier is nothing by default and extension is `jar` by default.

For global libraries (without `local` hint), the format translates to path:
```
libraries/<group with dots replaced by />/<name>/<version>/<name>-<version>[-<classifier>].<extenstion>
```

For example `com.mumfrey:liteloader:1.7.2_04` means:
```
libraries/com/mumfrey/liteloader/1.7.2_04/liteloader-1.7.2_04.jar
```

`com.mumfrey:liteloader:1.7.2_04:foo@zip` means:
```
libraries/com/mumfrey/liteloader/1.7.2_04/liteloader-1.7.2_04-foo.zip
```

Local libraries reside inside instances and the name translates to:
```
$instance/libraries/<name>-<version>[-<classifier>].<extenstion>
```

#### url

A base URL for downloading the library.

#### natives

The `natives` key provides a string for each specific platform to be used as the classifier. This allows having different versions of a library on different operating systems.

#### rules

The rules key is used to determine if the library is to be used at all or not.

#### MMC-absoluteUrl

This specifies the exact URL to download the library from.

#### MMC-hint

This can have three different values:
* `local` - MultiMC will load the library from inside the instance (`$Instance/libraries/$library.jar`) and will not try to download it.
* `always-stale` - MultiMC will always try to download a new version of the library.
* `forge-pack-xz` - the downloaded file should be post-processed using forge-specific rules.

# Additional information
Also see [here](http://wiki.vg/Game_Files) for some more information on the vanilla format (not used here, but closely related).

There used to be a file called `custom.json` that would completely override the content in a `version.json`. This made it hard to add/remove things like Forge and LiteLoader. The patches were originally created to solve this problem.

Later, this system was further extended to what it is now -- to support dependencies and automatic dependency resolving/checking.

Essentially, this evolved in parallel to the vanilla format, and often solved the same problem earliewr, and better. Sadly, this means that the formats have diverged and are no longer compatible (nor can they be made compatible).