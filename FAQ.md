### Is this a "pirated launcher"?
No. You need a premium Minecraft account, just like you do with the vanilla launcher. Yes, there's an offline mode, but it only works when you've successfully authenticated at least once with an account.

### How do I replace class files in my 1.6+ instance?
As of right now, you don't. Mojang have made it clear that they don't want people in the jar file, so we don't plan on supporting it. We will eventually, however, support loading custom libraries (our Forge integration is just a specific type of this). See [[Jarmodding]] for more information.

### Why does my 1.5.2 or older instance fail to load when I install Forge to it?
This is a Forge issue which we'll have a workaround for soon (they have a set of libraries that you need to manually download). For now, please read their EAQ (the bit about failed downloads in the "common problems and solutions section").

### Why don't the window icon, window title, maximise, and fullscree options work in 1.6 or newer?
We haven't implemented support for that yet, but we do plan on having it.

### Why can't I select a version of Minecraft over 1.5.2?
You're probably using MultiMC 4. Mojang fundamentally changed the way Minecraft is launched in later versions, and we decided to rewrite MultiMC to support it. You can get MultiMC 5 (which supports everything the vanilla launcher does) from the homepage.

### Where do I put my coremods in 1.6 or newer?
Forge now expects coremods to be in the same place as regular mods, so just stick them in the "Loader Mods" tab along with the other mods.

### Why do I get an SSL error (or why can't log in) using Windows XP?
Windows XP is really, really old now, but MultiMC will work on it provided you have both updated root certificates and MSVCR 2008 installed.
