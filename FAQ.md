### Is this a "pirated launcher"?
No. You need a premium Minecraft account, just like you do with the vanilla launcher. Yes, there's an offline mode, but it only works when you've successfully authenticated at least once with an account.

### How do I replace class files in my 1.6+ instance?
While this is possible, we would like to discourage the use of jar mods. Mojang have made it clear that they don't want people in the jar file. See [[Jarmodding]] for more information.

If you still need to do so, go to Instance Settings -> Versions -> Add jarmod

### Why don't the window icon, window title, maximise, and fullscreen options work in-game?
This can be changed in the instance settings per instance or in the multicraft settings for all the instances.

### Why can't I select a version of Minecraft over 1.5.2?
You're probably using MultiMC 4. Mojang fundamentally changed the way Minecraft is launched in later versions, and we decided to rewrite MultiMC to support it. You can get MultiMC 5 (which supports everything the vanilla launcher does) from the [homepage](http://multimc.org/).

### Where do I put my coremods in 1.6 or newer?
Forge now expects coremods to be in the same place as regular mods, so just stick them in the "Loader Mods" tab along with the other mods.

### Why do I get an SSL error (or why can't log in) using Windows XP?
Windows XP is really, really old now, but MultiMC will work on it provided you have both updated root certificates and MSVCR 2008 installed.

### Why am I getting weird crashes and/or slow rendering with a NVidia Optimus graphics card on Windows?
There's some blackmagic going on here, try renaming MultiMC.exe to Minecraft.exe.