If you have received the following error:
```
Terminating app due to uncaught exception 'NSInternalInconsistencyException', reason: 'NSWindow drag regions should only be invalidated on the Main Thread!'
```
on macOS when starting Minecraft, you will have to install an older version of Java.

To do so:
* First, uninstall the currently installed Java version, following this guide: https://explainjava.com/uninstall-java-macos/
* Then download and install this package: https://files.multimc.org/downloads/jre-8u241-macosx-x64.dmg
* After selecting the newly installed Java, you should be able to play normally.