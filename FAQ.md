## Minecraft not launching
There are many issues possible for this, here are some issues and solutions.

#### Mods are a different version
Makes sure that all the mods for the instance you are launching are for the version of Minecraft you're launching -- eg. 1.6.4 mods for Minecraft 1.6.4, 1.7.10 mods for Minecraft 1.7.10 and so on.

#### Putting forge/LiteLoader mods in jar mods instead of loader mods
Whether you're loading forge mods or LiteLoader mods, they all need to be added via. loader mods. Jar mods are added to the Minecraft jar, and that is a rare occurrence with most recent mods.

## Graphics issues

### Hybrid laptop graphics (optimus and similar)
If you get slow rendering and Minecraft using the integrated graphics card instead of the dedicated one, there are some ways to fix that:

#### Windows
Rename `MultiMC.exe` to `Minecraft.exe`. In general, the graphics drivers look for the binary name in order to enable the dedicated GPU. This fools them into enabling it.

The same applies to many other situations where graphics are an issue on Windows: Rename the .exe and it might just work better.

#### Linux
You can use the [Wrapper command option in the Java settings](https://github.com/MultiMC/MultiMC5/wiki/Java-settings#custom-commands) together with `optirun` or similar wrappers.

## Can't log in
Minecraft login can be blocked by several issues:

#### You changed your account name recently
In MultiMC, remove your Mojang account and add it again.

#### Network blocking or Mojang servers being down
Generally, you can detect this by looking at the status icons on the lower right of the MultiMC window. Clicking them leads to [The Mojang help page.](https://help.mojang.com/). If the auth and session servers are having issues, you just have to wait. If you can access the page, but the status icons show as offline, or if both are offline, your network access might be broken or filtered. We can't help you with that.

#### Secure access problems
If the access to the Mojang auth servers is compromised or impossible, you will get a scary error message. Please report these as bugs, along with uploading the MultiMC log file (MultiMC-0.log).