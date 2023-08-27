Generally you should use Java with the same architecture as your CPU. There are different version requirements for different Minecraft versions.
If you don't know which one and how to get it, read on. After you installed the correct version make sure [to select it](#setting-up-java-in-multimc).

# Windows  
    
### **Minecraft 1.17 and newer**

Pick the JRE versions and make sure to match the architecture with your system, usually x64 (64-bit)

Azul: <https://www.azul.com/downloads/?version=java-17-lts&os=windows&architecture=x86-64-bit&package=jre>
<details>
<summary>Other Distributions</summary>

* Eclipse Temurin: <https://adoptium.net/temurin/releases/?version=17>
  * Select in the dropdowns "Windows" "x64" "JRE" and "17"
* Microsoft OpenJDK: <https://docs.microsoft.com/en-gb/java/openjdk/download>
* Oracle: <https://www.oracle.com/java/technologies/downloads/#java17>
</details>   
&nbsp;

### **Minecraft 1.16 and older**

Pick the JRE versions and make sure to match the architecture with your system, usually x64 (64-bit)

Note: There is an exception when using some poorly supported/unsupported old integrated GPUs from Intel. See [[Unsupported-Intel-GPUs]] for details.

Azul: <https://www.azul.com/downloads/?version=java-8-lts&os=windows&architecture=x86-64-bit&package=jre>
<details>
  <summary>Other Distributions</summary>

* Eclipse Temurin: <https://adoptium.net/temurin/releases/?version=8>
  * Select in the dropdowns "Windows" "x64" "JRE" and "8"
* Java.com: <https://www.java.com/en/download/manual.jsp>
  * Make sure to download only the "_Windows Offline (x64)_" installer as Online can cause installation issues.  
![](https://cdn.discordapp.com/attachments/404818598541000704/681278632811036714/correct-windows-java.png)
</details>

&nbsp;

#  macOS #  

### **Minecraft 1.17 and newer**


Azul: <https://www.azul.com/downloads/?version=java-17-lts&os=macos&architecture=x86-64-bit&package=jre>
For least amount of issues, choose **.dmg** download.

**Native ARM Java is currently not supported on MultiMC.**

` Alternatively the Windows links above usually also provide macOS and Linux versions. On M1 Macs you need to make sure to get the x86_64 packages, native Arm Java is currently not supported! `


### **Minecraft 1.16 and older**

* Go to <https://www.java.com/en/download/manual.jsp>
* Download the `Mac OS X` package.
* Install it.

&nbsp;

# Linux


### **Minecraft 1.17 and newer**

Install the right package
* Ubuntu/Debian derivatives: `openjdk-17-jre`
* Arch `jre17-openjdk`
* Fedora `java-17-openjdk`
* OpenSUSE: `java-17-openjdk`





### **Minecraft 1.16 and older**

Install the right package

* Ubuntu/Debian derivatives: `openjdk-8-jre`
* Arch `jre8-openjdk`
* Fedora `java-1.8.0-openjdk`
* OpenSUSE: `java-1.8.0-openjdk`

### **Common issue is that people install only the headless version, and then it doesn't work. Make sure you have the full desktop version. Headless is for servers.**

&nbsp;


&nbsp;


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
