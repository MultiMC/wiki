This is quite a big topic. It will be assumed that you are familiar with opening files, the JSON file format, and that you know how to ask for help, and when to not ask at all.

This entire page only applies to 1.6+.

Also see [here](http://wiki.vg/Game_Files) for some more information

### What are patches?

There used to be a file called custom.json that would completely override the content in version.json. This made it hard to add/remove things like Forge and LiteLoader. Now there exist so called "patches" that are applied on top of version.json.

Patches are stored in `<instance>/patches/<name>.json`, where `<name>` should be a Java package-style descriptor, for example `net.minecraftforge` or `com.mumfrey.liteloader`.

## Format

The format of patches are similar to that of the vanilla version.json, but with some additions.

Lets start with the LiteLoader patch as an example:

```json
{
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
            "MMC-absoluteUrl": "http://dl.liteloader.com/versions/com/mumfrey/liteloader/1.7.2/liteloader-1.7.2_04.jar",
            "MMC-depend": "hard",
            "insert": "prepend",
            "name": "com.mumfrey:liteloader:1.7.2_04"
        }
    ],
    "+tweakers": [
        "com.mumfrey.liteloader.launch.LiteLoaderTweaker"
    ],
    "fileId": "com.mumfrey.liteloader",
    "mainClass": "net.minecraft.launchwrapper.Launch",
    "mcVersion": "1.7.2",
    "name": "LiteLoader",
    "order": 10,
    "version": "1.7.2_04"
}
```
### Metadata fields

These fields are only for sorting of patches, and for displaying to the user, and don't affect the general game.

| Field | Description |
| --- | --- |
| fileId | Should be the same as the `<name>` of the file |
| mcVersion | Which version of Minecraft this patch is for |
| name | A human-readable version of the name |
| order | Used for sorting patches, lower number means applied earlier. Patches may NOT have the same order |
| version | The version of this patch, or the the library it is for |

### Other fields

These fields actually affect the launching of the game. Some can be added to or removed from using `+` or `-` before the field name, while others can only be overwritten. No + or - means overwrite.

| Field | +/- allowed | Description |
| --- | --- | --- |
| mainClass | No | This is the name of the Java class that will be launched. This is used by Launchwrapper to place give it access to the game loading |
| tweakers | Yes | WITH LAUNCHWRAPPER ONLY: A list of tweakers (passed to Minecraft with `--tweakClass` |
| libraries | Yes | A list of libraries (dependencies) used by the game. See below for more info |
| minecraftArguments | Yes | The arguments passed to Minecraft |
| id | No | Specifies which version jar to use |
| time | No | |
| releaseTime | No | |
| type | No | |
| processArguments | No | |
| minimumLauncherVersion | No | Which launcher version is needed as a minimum |


### libraries

The `libraries` list contains a list of objects with the following possible fields.

`name` is the only field that is required

| Field | Description |
| --- | --- |
| name | `<group>:<name>:<version>` means the library at `libraries/<group with dots replaced by />/<name>/<version>/<name>-<version>.jar`, for example `com.mumfrey:liteloader:1.7.2_04` means `libraries/com/mumfrey/liteloader/1.7.2_04/liteloader-1.7.2_04.jar`
| url | A base URL for downloading the library. |
| natives | The natives key provides a string for each specific platform to be inserted between the .jar and the `<version>` of the filename. |
| extract | The extract key provides rules for the extraction of the file. |
| rules | The rules key is used to determine which platforms to download the file to. When the action is allow, the file will be downloaded to the platform stated in os. When the action is disallow, the file will not be downloaded to the platform stated in os. If there is no os key, the rule is default for non-specified platforms. |
| MMC-absoluteUrl | If the remote location of the library doesn't fit the standard, one can use this to specify the full URL |
| MMC-hint | This can have two different values: `local` means MultiMC will not try to (re)download the library, `forge-pack-xz` means that the downloaded file should be extracted using magic |
| insert | Required with `+libraries`, specifies how the library should be applied. See below for more info. |
| MMC-depend | Required with some `insert` types (append and prepend). See below for more info. |

#### `insert`

**`apply`:** Used for adding/changing information about a library, the information contained in this object will override and augment those already available.<br/>
**`replace`:** Entirely override the existing library with the information contained in this object<br/>
**`prepend`:** Prepends the library if it does not exist already, acts like `apply` if it exists already<br/>
**`append`:** Same as `prepend`, but appends instead of prepends<br/>

#### `MMC-depend`

The value of `MMC-depend` is used when the `insert` type is `append` or `prepend` to decide what other libraries count as the same, regarding the version.

**`hard`:** This version of the library is required, and no other is allowed.
**`soft`:** At least this version of the library is required, but higher versions are allowed.

If library dependencies cannot be resolved (for example if there are two different hard dependencies, or a hard dependency that is below a soft dependency) the loading of the instance will fail.