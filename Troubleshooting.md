Having some issues? here are some common issues and the solutions to them.

## "Failed to create virtual machine"
This probably means you're trying to run Minecraft with 32 bit java and have set more than 1GB of ram. Go checkout [[Increasing Java's memory allocation]]

## Minecraft not launching
Here are some common issues preventing minecraft from launching,

#### Mods are a different version
Makes sure that all the mods for the instance you are launching is for the version of mc your launching. eg 1.6 mods for mc 1.6, 17 mods for mc 1.7

#### Putting forge/Liteloader mods in jar mods instead of loader mods
Whether you're loading forge mods or liteloader mods, they all need to be added via. loader mods, jar mods are added to the minecraft jar, which only forge=, liteloader & mods **that specifically specify** to be put in the mc jar.

***
Still having issues or your problem isn't listed here? Go and search for your problem [here](https://github.com/MultiMC/MultiMC5/issues) & see if someone else has the same issue. Still no luck? Make a new [issue](https://github.com/MultiMC/MultiMC5/issues/new) & include your log. Make sure to use the upload button when reporting a bug!