Generally you should use Java with the same architecture as your CPU. There are different version requirements for different Minecraft versions.
If you don't know which one and how to get it, read on. After you installed the correct version make sure [to select it](#setting-up-java-in-multimc).

# Windows  

### **Minecraft 1.20.5 and newer (Java 21)**

**Make sure to download the .msi installer!**

Eclipse Temurin: <https://adoptium.net/temurin/releases/?os=windows&arch=x64&package=jre&version=21>

&nbsp;

### **Minecraft 1.17 until 1.20.4 (Java 17)**

Pick the JRE versions and make sure to match the architecture with your system, usually x64 (64-bit)

**Make sure to download the .msi installer!**

Eclipse Temurin: <https://adoptium.net/temurin/releases/?os=windows&arch=x64&package=jre&version=17>

Scroll down until you see the single entry in the table!
<details>
<summary>Other Distributions</summary>

* Azul: <https://www.azul.com/downloads/?version=java-17-lts&os=windows&architecture=x86-64-bit&package=jre>
* Microsoft OpenJDK: <https://docs.microsoft.com/en-gb/java/openjdk/download>
* Oracle: <https://www.oracle.com/java/technologies/downloads/#java17>
</details>

&nbsp;

### **Minecraft 1.16 and older (Java 8)**

Pick the JRE versions and make sure to match the architecture with your system, usually x64 (64-bit)

**Make sure to download the .msi installer!**

Note: There is an exception when using some poorly supported/unsupported old integrated GPUs from Intel. See [[Unsupported-Intel-GPUs]] for details.

Eclipse Temurin: <https://adoptium.net/temurin/releases/?os=windows&arch=x64&package=jre&version=8>

<details>
  <summary>Other Distributions</summary>

* Azul: <https://www.azul.com/downloads/?version=java-8-lts&os=windows&architecture=x86-64-bit&package=jre>
* Java.com: <https://www.java.com/en/download/manual.jsp>
  * Make sure to download only the "_Windows Offline (x64)_" installer as Online can cause installation issues.  
![](https://cdn.discordapp.com/attachments/404818598541000704/681278632811036714/correct-windows-java.png)
</details>
&nbsp;

#  macOS #
**M1/M2/M3 CPU: Native ARM Java is currently not supported on MultiMC and x86_64 packages are required.**

For least amount of issues, choose **.pkg** download.

### **Minecraft 1.20.5 and newer (Java 21)**
Eclipse Temurin: <https://adoptium.net/temurin/releases/?os=mac&arch=x64&package=jre&version=21>

&nbsp;

### **Minecraft 1.17 until 1.20.4 (Java 17)**
Eclipse Temurin: <https://adoptium.net/temurin/releases/?os=mac&arch=x64&package=jre&version=17>
  
  
&nbsp;

### **Minecraft 1.16 and older (Java 8)**

* Go to <https://www.java.com/en/download/manual.jsp>
* Download the `Mac OS X` package. Make sure to download the x64 as ARM is currently not supported.
* Install it.

&nbsp;

# Linux

### **Minecraft 1.20.5 and newer (Java 21)**

`temurin-21-jdk`


### **Minecraft 1.17 until 1.20.4 (Java 17)**

* Ubuntu/Debian derivatives: `openjdk-17-jre`
* Arch `jre17-openjdk`
* Fedora `java-17-openjdk`
* OpenSUSE: `java-17-openjdk`
&nbsp;

### **Minecraft 1.16 and older (Java 8)**

* Ubuntu/Debian derivatives: `openjdk-8-jre`
* Arch `jre8-openjdk`
* Fedora `java-1.8.0-openjdk`
* OpenSUSE: `java-1.8.0-openjdk`

**Do not choose the headless version as that is designed for servers and not general use.**
&nbsp;


&nbsp;
# Setting up Java in MultiMC

* In MultiMC, set it up using the `Auto detect` feature in the main settings - see [[Java-settings]] for details.
* See [[Increasing Java's memory allocation]] for more details about Java memory settings.

![](https://cdn.discordapp.com/attachments/531598137790562305/575378380573114378/unknown.png)

## Set Instance Java Installation

Go to **Edit Instance** -> **Settings** -> **Java** -> **Java Installation**.

![https://i.imgur.com/B9njIC1.png](https://i.imgur.com/B9njIC1.png)

## My Java Installation doesn't appear on the list, what do I do?

Try refreshing the list. If that fails, you'll need to locate the Java executable yourself - within the root Java directory this is `./bin/java` on Unix systems, and `.\bin\javaw.exe` on Windows.
