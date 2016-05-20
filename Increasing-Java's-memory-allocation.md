You can increase the amount of memory allocated to your Minecraft instance by going to the Java tab, in the Settings dialog, and altering the values in the Memory section.

In general, values of `1024 MB` minimum, `2048 MB` maximum and `128 MB` PermGen are adequate for modded instances, though you may need to increase this for larger instances. If you're using 32 bit java, please do note the max ram can be no higher than 1500MB. That's the likely problem, when you get `Failed to create virtual machine`.

If you use Java 8 or newer, the PermGen number no longer has any meaning. Just keep it at its default of 64.

If you get a `java.lang.OutOfMemoryError` exception when you try to run an instance, you probably need to increase the amount of memory allocated to it.

![Example memory settings](https://i.imgur.com/1PLWTtw.png)

For more information about this page, checkout [[java settings]]