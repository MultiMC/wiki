## Minecraft not launching
There are many issues possible for this, here are some issues and solutions.

#### Mods are a different version
Makes sure that all the mods for the instance you are launching are for the version of Minecraft you're launching -- eg. 1.6.4 mods for Minecraft 1.6.4, 1.7.10 mods for Minecraft 1.7.10 and so on.

#### Putting forge/LiteLoader mods in jar mods instead of loader mods
Whether you're loading forge mods or LiteLoader mods, they all need to be added via. loader mods. Jar mods are added to the Minecraft jar, and that is a rare occurrence with most recent mods.

#### Why am I getting weird crashes and/or slow rendering with a NVidia Optimus graphics card on Windows?
There's some black magic going on here, try renaming MultiMC.exe to Minecraft.exe.

## Can't log in
Minecraft login can be blocked by several issues:

#### You changed your account name recently
In MultiMC, remove your Mojang account and add it again.

#### Network blocking or Mojang servers being down
Generally, you can detect this by looking at the status icons on the lower right of the MultiMC window. Clicking them leads to [The Mojang help page.](https://help.mojang.com/). If the auth and session servers are having issues, you just have to wait. If you can access the page, but the status icons show as offline, or if both are offline, your network access might be broken or filtered. We can't help you with that.

#### Secure access problems
If the access to the Mojang auth servers is compromised or impossible, you will get a scary error message. Please report these as bugs, along with uploading the MultiMC log file (MultiMC-0.log).