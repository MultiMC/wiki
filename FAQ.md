### 1. _Is this a "pirated launcher"?_
No. You need a premium Minecraft account, just like you do with the vanilla launcher. Yes, there's an offline mode, but it only works when you've successfully authenticated at least once with an account.

### 2. _How do I replace <class file> in my 1.6+ instance?_
As of right now, you don't. Mojang have made it clear that they don't want people in the Jar, so we don't plan on supporting it. We will eventually, however, support loading custom libraries (our Forge integration is just a specific type of this). See [[Jarmodding]] for more information.

### 3. _Why does my <1.5.2 instance fail to load when I install Forge to it?_
This is a Forge issue which we'll have a workaround for soon (they have a set of libraries that you need to manually download). For now, please read their EAQ (the bit about failed downloads in the "common problems and solutions section").

### 4. _My \<window icon/window title/maximise/fullscreen\> options don't work in 1.6+_
We haven't implemented support for that yet, but we do plan on having it.

### 5. _Why can't I select a version of Minecraft over 1.5.2?_
You're probably using MultiMC 4. Mojang fundamentally changed the way Minecraft is launched in later versions, and we decided to rewrite MultiMC to support it. You can get MultiMC 5 (which supports everything the vanilla launcher does) from the homepage.

### 6. _Where do I put my coremods in 1.6+?_
Forge now expects coremods to be in the same place as regular mods, so just stick them in the "Loader Mods" tab along with the other mods.

### 7. _Why do I get an SSL error (or why can't log in) using Windows XP?_
Windows XP is really, really old now, but MultiMC will work on it provided you have both updated root certificates and MSVCR 2008 installed.
