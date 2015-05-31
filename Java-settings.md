Here you can set the global Java settings

## Memory

![](https://i.imgur.com/UQFcAKh.png)

Java memory settings. For explanation, see: [[Increasing Java's memory allocation]]

## Java Runtime
![](https://i.imgur.com/TNCsnRB.png)

This is where the settings for the Java runtime live, like the location of the runtime and any Java arguments to use.

**Auto-detect** will check your computer for all java versions and show you a list of them, the best one on top.

**Test** can be used to test the selected Java runtime along with your memory settings and JVM arguments without starting the game.

## Custom Commands
![](https://i.imgur.com/cS5dzDF.png)

**Pre-launch command** runs before the instance launches and **Post-exit command** runs after it exits.
Both will be run in MultiMC's working directory with INST_ID, INST_DIR, and INST_NAME as environment variables.

**Wrapper command** allows running java using an extra wrapper program (like `optirun` on Linux, for use with optimus graphics laptops)