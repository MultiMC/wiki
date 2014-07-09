# Instance settings
The instance settings allow you to override the global MultiMC settings for a particular instance.
The settings are divided in sections, each with a check box, which enables the override.

##Java installation
Here, you can either directly insert the java runtime you want to use, let MultiMC detect it automatically (probably the best option), look for it using a file browser and test the currently selected one.

If you use integrated intel graphics on Windows, make sure to select the javaw.exe executable, not java.exe!

## Memory settings
The MultiMC default memory settings are suitable for lightly modded instances or vanilla Minecraft. You might want to set the numbers higher (about double the default sizes is generally OK). With 32bit java, the maximum is around 1500MB.

##Java arguments
MultiMC generally adds most of the relevant JVM arguments itself. If you know what you are doing, you can add your own here. Advice about what is to be put here pops up on internet discussion forums, but most of the time, its effects are negligible or even harmful. You've been warned.

##Game window
Lets you override the Minecraft window size. The maximize option only works for legacy versions (1.5.2 and older).

##Console settings
Should be self-explanatory. If you want to watch the game start up or are trying to fix some mod problem, it's a good idea to enable the console and not let it close on game exit. The console is however always accessible -- you can find it as a tray icon that appears when you start an instance.

##Custom commands
These allow starting various commands on instance start or exit. The commands have to finish running for the instance start/exit to proceed.