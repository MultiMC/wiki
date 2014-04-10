There are two types settings: Global and per-instance
* Global settings are accessed by clicking the <img alt="Settings Button" src="images/SettingsButton.png" width="24px;"/>
* Per-instance settings are accessed by selecting an instance and then clicking _Settings_ in the right toolbar

Global settings contain settings common to all instances, MultiMC itself etc., while per-instance settings can be used to override some things individually for each instance.

Notes/warnings on some settings:

* Features
  * Update Settings -> Update Channel
    * Release candidates will not receive hotfixes that only are applied to stable and development
  * FTB
    * The auto-detected paths here are generally correct, though you may have to edit the Files path
* Java
  * Memory
    * This is the place to go if you get any errors mentioning "Out of memory", or if you are playing with many mods.
    * 32bit Java cannot take Min/Max allocation values over ~1500MB
    * In Java 8 the PermGen value is still passed to Minecraft, and might give a warning, though it's harmless
  * Java Settings -> JVM Arguments
    * This can be used for extra JVM Arguments. Do not put -Xmx, -Xms or -XX:PermSize here, use the Memory fields for that
  * Custom Commands
    * These can for example be used for updating your modpack, backing up your saves etc.
    * These are not for JVM arguments, use the _JVM Arguments_ field for that
    * The environment variables INST_NAME, INST_ID, INST_DIR, INST_MC_DIR, INST_JAVA, INST_JAVA_ARGS will be set when running the commands, these variables can also be used in the command string (Unix syntax, $\<variable name\>).
* External Tools
  * See [[External Tools]]