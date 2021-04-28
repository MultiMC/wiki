The right Java version to use is Java 8, with the same architecture as your CPU.
If you don't know how to get it, read on.

# Getting and installing Java 
## Linux

* Install the right package

  **Unbuntu/Debian derivatives**
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