The last section of the _Instance Actions_ menu allows for users to export their instances.

## Exporting an Instance
* select the instance you wish to export but do not launch it.
* Click _Export Instance_. This will bring up a new window asking which files to include in the export.

![](http://i.imgur.com/n6p6FBv.png)

Exported instances will be saved in the zip format.

## Which Files are Necessary
By default, all the instance files are checked however not all of these are required in all minecraft launchers. The following will explain the basics of each file shown above:

* /patches: where mod-loaders are loaded from such and Forge and Liteloader. Most other launchers have their own way of doing this so would only be necessary for importing back into MultiMC.
* /minecraft: where all of the essential minecraft data is stored and is required for minecraft to launch correctly. This includes loader mods and config options.
* /jarmods: where mods that would normally go into the minecraft.jar are stored. Most other launchers would require you to add these manually. Should only be used for importing back into MultiMC.
* /order.json: required to specify the order in which the instance version components launch in.
* /instance.cfg: This is a MultiMC only feature that is made for the launcher and thus has no use in other launchers. Typically this is client side and does not need to be distributed to other players.

## Importing in MultiMC

You can import any zipped modpacks that are already made for MultiMC as _.zip_ files.
Learn more about importing here: **[[Import Instance]]**.