MultiMC has built-in support for a few Minecraft and Java related tools. If you'd like another tool added then [create a feature request](Feedback).

For most tools you will need to tell MultiMC where to find them. To do that click <img alt="Settings Button" src="images/SettingsButton.png" width="24px;"/>, go to _External Tools_ and enter the path.

To run a tool, either right click the instance, click _Play_ and then select the tool, or hold the _Play_ button in the instance toolbar clicked for a few seconds until the same menu pops up. Some tools, like profilers, will launch the game, while others won't.

## JProfiler

> JProfiler's intuitive UI helps you resolve performance bottlenecks, pin down memory leaks and understand threading issues.

After clicking _JProfiler_ in the _Play_ menu a JProfiler server will be started up at port 42042. You then need to manually start JProfiler and you should be able to connect to the local server, setup everything, and then click _Launch_ in the dialog that MultiMC opens.

## JVisualVM

> Java VisualVM is an intuitive graphical user interface that provides detailed information about Java technology-based applications (Java applications) while they are running on a given Java Virtual Machine (JVM*). The name Java VisualVM comes from the fact that Java VisualVM provides information about the JVM software visually.
Java VisualVM combines several monitoring, troubleshooting, and profiling utilities into a single tool. For example, most of the functionality offered by the standalone tools jmap, jinfo, jstat and jstack have been integrated into Java VisualVM. Other functionalities, such as some of those offered by the JConsole tool, can be added as optional plug-ins.

After clicking _JVisualVM_ in the _Play_ menu JVisualVM will be launched. Take your time to set it up, the launch of Minecraft will be delayed until you click Launch in the dialog that MultiMC opens.

To get you started, go to the _Sampler_ tab and select _CPU_. Then click _Launch_ in the MultiMC dialog.

## MCEdit

> MCEdit is an open source world editor for the popular game Minecraft. MCEdit was first created to allow players to preserve anything built with several old versions of Minecraft and take them forward into newer versions of the game. It also aims to be forward-compatible with future (or even modified) versions of Minecraft. It has since been improved with brush tools for laying down blocks in different shapes, integration with the Minecraft Server to generate terrain using Minecraft’s own seed algorithms, support for multiplayer worlds, and editors for certain blocks including chests and mob spawners.

Get MCEdit [here](http://www.mcedit.net/)

After clicking _MCEdit_ in the _Play_ menu you will be prompted for which world to open. After doing that you will be launched straight into that world in MCEdit