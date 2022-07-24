Generally you should use Java with the same architecture as your CPU. There are different version requirements for different Minecraft versions.
If you don't know which one and how to get it, read on. After you installed the correct version make sure [to select it](#setting-up-java-in-multimc).

# Minecraft 1.17 and newer

For Minecraft 1.17 you need to use at least Java 16, for 1.18 you need to use Java 17 so it's easiest to just install Java 17 for both.

## Linux

Install the right package

* Ubuntu/Debian derivatives: `openjdk-17-jre`
* Arch `jre17-openjdk`
* Fedora `java-latest-openjdk`
* OpenSUSE: `java-17-openjdk` (currently only in Tumbleweed)

## Windows

Pick the JRE versions and make sure to match the architecture with your system, usually x64 (64-bit)

* Azul: https://www.azul.com/downloads/?version=java-17-lts&os=windows&architecture=x86-64-bit&package=jre#download-openjdk
* Eclipse Adoptium: https://adoptium.net/?variant=openjdk17&jvmVariant=hotspot
* Microsoft OpenJDK: https://docs.microsoft.com/en-gb/java/openjdk/download
* Oracle: https://www.oracle.com/java/technologies/downloads/#java17


## macOS

- Homebrew: `openjdk@17`
- Macports: `openjdk17`

Alternatively the Windows links above usually also provide macOS and Linux versions. On M1 Macs you need to make sure to get the x64 packages, native Arm Java is currently not supported!


# Minecraft 1.16 and older

The right Java version to use is Java 8

## Linux

* Install the right package

  **Ubuntu/Debian derivatives**
  ```
  # apt-get install openjdk-8-jre
  ```
  **Arch**
  ```
  # pacman -Syu jre8-openjdk
  ```
  **RPM-based distributions**
  ```
  # yum install java-1.8.0-openjdk
  ```

Common issue is that people install only the headless version, and then it doesn't work. Make sure you have the full desktop version. Headless is for servers.

## Windows

Note: There is an exception when using some poorly supported/unsupported old integrated GPUs from Intel. See [[Unsupported-Intel-GPUs]] for details.

### 64-bit
* Go to https://www.java.com/en/download/manual.jsp
* Download the `Windows Offline (64-bit)` installer, as shown below.
![](https://cdn.discordapp.com/attachments/404818598541000704/681278632811036714/correct-windows-java.png)
* Install it.

### 32-bit
* Go to https://www.java.com/en/download/manual.jsp
* Download the `Windows Offline` installer.
* Install it.

You will be limited to roughly 1500MB Java heap size, which is not big enough for mods in most cases.

## macOS
* Go to https://www.java.com/en/download/manual.jsp
* Download the `Mac OS X ` package.
* Install it.

# Setting up Java in MultiMC

* In MultiMC, set it up using the `Auto detect` feature in the main settings - see [[Java-settings]] for details.
* See [[Increasing Java's memory allocation]] for more details about Java memory settings.

![](https://cdn.discordapp.com/attachments/531598137790562305/575378380573114378/unknown.png)

## Set Instance Java Installation

Go to **Edit Instance** -> **Settings** -> **Java** -> **Java Installation**.

![https://i.imgur.com/B9njIC1.png](https://i.imgur.com/B9njIC1.png)

## My Java Installation doesn't appear on the list, what do I do?

Try refreshing the list. If that fails, you'll need to locate the Java executable yourself - within the root Java directory this is `./bin/java` on Unix systems, and `.\bin\javaw.exe` on Windows.
