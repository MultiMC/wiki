# Creating Instance Shortcuts
![create shortcut screen](https://user-images.githubusercontent.com/35371030/177705677-8399ad6f-da12-4adc-bc20-dbc845a637b1.png)


MultiMC offers the ability to create a shortcut file that will directly launch a specific instance when opened.
To get started, right click on an instance and press 'Create Shortcut', or select an instance and press 'Create Shortcut' on the sidebar on the right.
The window shown at the top of this page will open.


![create shortcut buttons](https://user-images.githubusercontent.com/35371030/177706235-c87668c0-a250-47c4-be46-4ad6fb71920e.png)

## Note for Mac users:
macOS does not have a concept of a shortcut in the same way as Windows or some Linux distributions, so this option will always create a shell script instead.
For more information, see [Create script instead of shortcut](#create-script-instead-of-shortcut).

## Options
### Shortcut path
This is the file that the shortcut will be saved as. The default location is a file on your desktop called "Instance Name - MultiMC 5".
You can change the file location to wherever you want; the correct file extension for your platform will be added automatically.

### Join server on launch
This allows you to join a specific Minecraft server as soon as the game is launched. Enable the checkbox and type the server's address or IP in the text box next to it.
Note: This option is disabled for certain versions of the game due to bugs [MC-145102](https://bugs.mojang.com/browse/MC-145102) and [MC_228828](https://bugs.mojang.com/browse/MC-228828) which caused the game to crash with this option enabled.

### Use specific profile
This option allows you to select a certain account to launch the instance with. Enable the checkbox and select the account you want to use from the menu.

### Launch in offline mode
This allows you to launch an instance in 'offline mode', the same as if you used the 'Launch Offline' button in MultiMC's GUI.
In offline mode, you can play without an internet connection and use a different username, but you will not be able to join most servers.
Note: This does not allow you to play the game without buying it. MultiMC will not launch in offline mode if you do not have a valid account added.
#### Set offline mode username
If the 'launch in offline mode' checkbox is enabled, this allows you to set a custom username.
This only functions in offline mode; if you want a different username in online mode you will need to change it through the Minecraft website.

### Create script instead of shortcut
By default, a shortcut (.desktop file on Linux) will be created.
If this option is enabled, a shell script (Linux/Mac) or batch file (Windows) will be created instead.
Note that this option is force-enabled on Mac, because macOS does not have shortcuts in the same way as Windows.
You will also have to use this if you use a Linux distribution or desktop environment that does not support .desktop files.

## Finishing Up
To create the shortcut, press the OK button. A shortcut will be created in the specified location with the specified options.
If you press Cancel or close the window, no files will be created or overwritten.
