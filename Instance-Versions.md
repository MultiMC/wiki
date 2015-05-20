![](http://i.imgur.com/HdZXaSL.png)
***
Here, you can add the various components that make up the base of the instance and change their versions.
## Selection

* **Change Version**: Almost all minecraft versions available can be selected. This includes releases, snapshots and even alpha and beta releases. Changing the Minecraft version will also remove/replace all the other base components such as mod-loaders like Forge or Liteloader.

* **Move Up/Down**: These buttons are for more advanced users who want to customize in which order the components are launched. Minecraft and LWJGL should always be the first two on the list. This is mostly used for re-ordering jar mods.

* **Remove**: Can be used to remove any added jar mod or mod-loader. Do not remove Minecraft or LWJGL. These are required for the game to launch.
## Edit

  * **Customize**: Advanced users can customize the .json file that loads their minecraft instance. In general these files should not be touched unless you know what you are doing. Messing one of these up could mean having to delete your instance and recreate it.

  * **Edit**: Opens the selected file using the default file editor for that type of file on the operating system. Edit is only available if the version is customized. By default, all installed mod-loaders are classified as custom versions.

  * **Revert**: By default, MultiMC stores a copy of the original, un-customized file so if you no longer wish to keep saved changes to the .json file, they can be restored to the original versions.

##Install

  * **Install Forge/Liteloader**: These install buttons are *THE ONLY* way to install Forge and LiteLoader in MultiMC. Their original installers do not work here. Advanced used can edit these mod-loaders (see editing components above).

  * **Add Jar Mod**: Mods that you would normally have to add to the minecraft jar file can be added here. In general, these should be added below the mod-loaders that you have installed. Typically if there is an issue while launching with jar mods, try re-ordering them with the 'Move up' and 'Move down' buttons to see if one overrides the other. Mods lower in the list override the ones above them. Now days, most mods should be installed in the mods folder and use a mod-loader to launch.
##List

  * **Reset Order**: Reset the order of the installed versions to the order that it was first installed in.
  
  * **Reload**: Refreshes the version list from the patches folder in the instance folder. This is helpful if a user has made edits to the files while MultiMC is open.