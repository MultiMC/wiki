The instance settings allow you to override the global MultiMC settings for a particular instance.
The settings are divided in sections, each with a check box, which enables the override.

##Java installation
![](http://dethware.org/pics/mmchelp/javainst.png)

Here, you can either directly insert the java runtime you want to use, let MultiMC detect it automatically (probably the best option), look for it using a file browser and test the currently selected one.

If you use integrated intel graphics on Windows, make sure to select the javaw.exe executable, not java.exe!

## Memory settings
![](http://dethware.org/pics/mmchelp/javamem.png)

The MultiMC default memory settings are suitable for lightly modded instances or vanilla Minecraft. You might want to set the numbers higher (about double the default sizes is generally OK). With 32bit java, the maximum is around 1500MB.

##Java arguments
![](http://dethware.org/pics/mmchelp/javaargs.png)

MultiMC generally adds most of the relevant JVM arguments itself, without any need for adding more. If you know what you are doing, you can add some here. Advice about what is to be put here pops up on internet discussion forums, but most of the time, its effects are negligible or even harmful. You've been warned.

##Game window
![](http://dethware.org/pics/mmchelp/windowopts.png)

Lets you override the Minecraft window size. The maximize option only works for legacy versions (1.5.2 and older).

##Console settings
![](http://dethware.org/pics/mmchelp/consoleopts.png)

Should be self-explanatory. If you want to watch the game start up or are trying to fix some mod problem, it's a good idea to enable the console and not let it close on game exit. The console is however always accessible -- you can find it as a tray icon that appears when you start an instance, even with these options disabled.

##Custom commands
![](http://dethware.org/pics/mmchelp/custcmds.png)

Pre-launch command runs before the instance launches and post-exit command runs after it exits. The commands run in MultiMC's working directory with INST_ID, INST_DIR and INST_NAME as environment variables.

The commands have to finish running for the instance start/exit to proceed.

If this means nothing to you, you can safely ignore these options.