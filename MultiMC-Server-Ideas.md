An often requested feature for MultiMC is the addition of a server handling part. See issue #60.

This page is for collecting ideas of what could be included in a possible MultiMC Server, as well as ideas of how it can be implemented.

## Feature Ideas

* Starting and stopping of servers
* Handling of files (mod lists)
* Changing Minecraft (and other) versions
* Support for [Cauldron](http://cauldron.minecraftforge.net/) (see #385) and Forge
* Sync a server instance with a client instance (for things like starting, stopping and Minecraft version)
* QuickMod support
* Real-time transfer of logs

## Implementation details

* SSH for control
* FTP for file transfers
* Should re-use as much of the code in logic/ as possible. Will require refactors to get rid of GUI code in logic/