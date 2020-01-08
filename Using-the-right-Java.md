The right Java version to use is Java 8, with the same architecture as your CPU.
If you don't know how to get it, read on.

# Linux

* Install the right package

  **Unbuntu/Debian derivatives**
  ```
  # apt-get install openjdk-8-jre
  ```
  **Arch**
  ```
  # pacman -Sy jre8-openjdk
  ```
  **RPM-based distributions**
  ```
  # yum install java-1.8.0-openjdk
  ```
* In MultiMC, set it up using the `Auto detect` feature in the main settings - see [[Java-settings]] for details.
* See [[Increasing Java's memory allocation]] for more details about Java memory settings.

Common issue is that people install only the headless version, and then it doesn't work. Make sure you have the full desktop version. Headless is for servers.

# Windows

* Go to https://www.java.com/en/download/manual.jsp
* Download the `Windows Offline (64-bit)` installer, if your CPU is 64bit.
* Download the `Windows Offline` installer, if your CPU is 32bit - you will be limited to roughly 1500MB Java heap size, which is not big enough for mods in most cases.
* Install it.
* In MultiMC, set it up using the `Auto detect` feature in the main settings - see [[Java-settings]] for details.
* See [[Increasing Java's memory allocation]] for more details about Java memory settings.

There is an exception when using some poorly supported/unsupported old integrated GPUs from Intel. See [[Unsupported-Intel-GPUs]] for details.

# macOS
* Go to https://www.java.com/en/download/manual.jsp
* Download the `Mac OS X ` package.
* Install it.
* In MultiMC, set it up using the `Auto detect` feature in the main settings - see [[Java-settings]] for details.
* See [[Increasing Java's memory allocation]] for more details about Java memory settings.
