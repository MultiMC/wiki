Generally you should use Java with the same architecture as your CPU. There are different version requirements for different Minecraft versions.
If you don't know which one and how to get it, read on. After you installed the correct version make sure [to select it](#setting-up-java-in-multimc).

# Windows  

### **Minecraft 26 and newer (Java 25)**

**Make sure to download the .msi installer!**

Eclipse Termurin: <https://adoptium.net/temurin/releases/?os=windows&arch=any&package=jre&version=25&mode=filter>

Scroll down until you see the single entry in the table!
<details>
<summary>Other Distributions</summary>

* Azul: <https://www.azul.com/downloads/?version=java-25-lts&os=windows&architecture=x86-64-bit&package=jre#zulu>
* Microsoft OpenJDK: <https://learn.microsoft.com/en-gb/java/openjdk/download#openjdk-25>
* Oracle: <https://www.oracle.com/java/technologies/downloads/#jdk25-windows>
</details>

&nbsp;

### **Minecraft 1.20.5 until 1.21.11 (Java 21)**

**Make sure to download the .msi installer!**

Eclipse Temurin: <https://adoptium.net/temurin/releases/?os=windows&arch=x64&package=jre&version=21>

Scroll down until you see the single entry in the table!
<details>
<summary>Other Distributions</summary>

* Azul: <https://www.azul.com/downloads/?version=java-21-lts&os=windows&architecture=x86-64-bit&package=jre#zulu>
* Microsoft OpenJDK: <https://learn.microsoft.com/en-gb/java/openjdk/download#openjdk-21>
* Oracle: <https://www.oracle.com/java/technologies/downloads/#jdk21-windows>
</details>

&nbsp;

### **Minecraft 1.17 until 1.20.4 (Java 17)**

Pick the JRE versions and make sure to match the architecture with your system, usually x64 (64-bit)

**Make sure to download the .msi installer!**

**MCSR Users:** Must use this version

Eclipse Temurin: <https://adoptium.net/temurin/releases/?os=windows&arch=x64&package=jre&version=17>

Scroll down until you see the single entry in the table!
<details>
<summary>Other Distributions</summary>

* Azul: <https://www.azul.com/downloads/?version=java-17-lts&os=windows&architecture=x86-64-bit&package=jre>
* Microsoft OpenJDK: <https://learn.microsoft.com/en-gb/java/openjdk/download#openjdk-17>
* Oracle: <https://www.oracle.com/java/technologies/downloads/#java17-windows>
</details>

&nbsp;

### **Minecraft 1.16 and older (Java 8)**

Pick the JRE versions and make sure to match the architecture with your system, usually x64 (64-bit)

**Make sure to download the .msi installer!**

Note: There is an exception when using some poorly supported/unsupported old integrated GPUs from Intel. See [[Unsupported-Intel-GPUs]] for details.

Eclipse Temurin: <https://adoptium.net/temurin/releases/?os=windows&arch=x64&package=jre&version=8>

Scroll down until you see the single entry in the table!
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

### **Minecraft 26 and newer (Java 25)**

**Make sure to download the .msi installer!**

Eclipse Termurin: <https://adoptium.net/temurin/releases/?os=mac&arch=x64&package=jre&version=25&mode=filter>

Scroll down until you see the single entry in the table!
<details>
<summary>Other Distributions</summary>

* Azul: <https://www.azul.com/downloads/?version=java-25-lts&os=macos&architecture=x86-64-bit&package=jre#zulu>
* Microsoft OpenJDK: <https://learn.microsoft.com/en-gb/java/openjdk/download#openjdk-25>
* Oracle: <https://www.oracle.com/java/technologies/downloads/#jdk25-mac>
</details>

&nbsp;

### **Minecraft 1.20.5 until 1.21.11 (Java 21)**
Eclipse Temurin: <https://adoptium.net/temurin/releases/?os=mac&arch=x64&package=jre&version=21>

Scroll down until you see the single entry in the table!
<details>
<summary>Other Distributions</summary>

* Azul: <https://www.azul.com/downloads/?version=java-21-lts&os=macos&architecture=x86-64-bit&package=jre#zulu>
* Microsoft OpenJDK: <https://learn.microsoft.com/en-gb/java/openjdk/download#openjdk-17>
* Oracle: <https://www.oracle.com/java/technologies/downloads/#java17-mac>
</details>

&nbsp;

### **Minecraft 1.17 until 1.20.4 (Java 17)**
**MCSR Users:** Must use this version

Eclipse Temurin: <https://adoptium.net/temurin/releases/?os=mac&arch=x64&package=jre&version=17>

Scroll down until you see the single entry in the table!
<details>
<summary>Other Distributions</summary>

* Azul: <https://www.azul.com/downloads/?version=java-21-lts&os=macos&architecture=x86-64-bit&package=jre#zulu>
* Microsoft OpenJDK: <https://learn.microsoft.com/en-gb/java/openjdk/download#openjdk-17>
* Oracle: <https://www.oracle.com/java/technologies/downloads/#java17-mac>
</details>
  
&nbsp;

### **Minecraft 1.16 and older (Java 8)**

Eclipse Temurin: <https://adoptium.net/temurin/releases/?os=mac&arch=any&package=jre&version=8&mode=filter>

Scroll down until you see the single entry in the table!
<details>
<summary>Other Distributions</summary>

* Azul: <https://www.azul.com/downloads/?version=java-8-lts&os=macos&architecture=x86-64-bit&package=jre#zulu>


* Go to <https://www.java.com/en/download/manual.jsp>
* Download the `Mac OS X` package. Make sure to download the x64 as ARM is currently not supported.
* Install it.
  </details>

&nbsp;

# Linux

### **Minecraft 26 and newer (Java 25)**

Open terminal and type the following based on your distro
* Ubuntu/Debian derivatives `sudo apt-get temurin-25-jdk`
* Arch `sudo pacman -S jdk25-openjdk`
* Fedora `sudo dnf install temurin-25-jdk`
* OpenSUSE `sudo zypper install temurin-25-jdk`

Eclipse Termurin: <https://adoptium.net/temurin/releases/?os=windows&arch=any&package=jre&version=25&mode=filter>

Scroll down until you see the single entry in the table!
<details>
<summary>Other Distributions</summary>

* Azul: <https://www.azul.com/downloads/?version=java-25-lts&os=windows&architecture=x86-64-bit&package=jre#zulu>
* Microsoft OpenJDK: <https://learn.microsoft.com/en-gb/java/openjdk/download#openjdk-25>
* Oracle: <https://www.oracle.com/java/technologies/downloads/#jdk25-linux>
</details>

&nbsp;

### **Minecraft 1.20.5 until 1.21.11 (Java 21)**

Open terminal and type the following based on your distro
* Ubuntu/Debian derivatives `sudo apt-get temurin-21-jdk`
* Arch `sudo pacman -S jdk21-openjdk`
* Fedora `sudo dnf install temurin-21-jdk`
* OpenSUSE `sudo zypper install temurin-21-jdk`

Eclipse Temurin: <https://adoptium.net/temurin/releases/?os=linux&arch=any&package=jre&version=21&mode=filter>

Scroll down until you see the single entry in the table!
<details>
<summary>Other Distributions</summary>

* Azul: <https://www.azul.com/downloads/?version=java-21-lts&os=linux&architecture=x86-64-bit&package=jre#zulu>
* Microsoft OpenJDK: <https://learn.microsoft.com/en-gb/java/openjdk/download#openjdk-21>
* Oracle: <https://www.oracle.com/java/technologies/downloads/#jdk21-linux>
</details>


### **Minecraft 1.17 until 1.20.4 (Java 17)**
**MCSR Users:** Must use this version

Open terninal and type the following based on your distro
* Ubuntu/Debian derivatives: `sudo apt-get install openjdk-17-jre`
* Arch `sudo pacman -S jre17-openjdk`
* Fedora `sudo dnf install java-17-openjdk`
* OpenSUSE: `sudo zypper install java-17-openjdk`

Or you can manually download it

Eclipse Temurin: <https://adoptium.net/temurin/releases/?os=linux&arch=any&package=jre&version=17&mode=filter>

Scroll down until you see the single entry in the table!
<details>
<summary>Other Distributions</summary>

* Azul: <https://www.azul.com/downloads/?version=java-17-lts&os=linux&architecture=x86-64-bit&package=jre#zulu>
* Microsoft OpenJDK: <https://learn.microsoft.com/en-gb/java/openjdk/download#openjdk-17>
* Oracle: <https://www.oracle.com/java/technologies/downloads/#jdk17-linux>
</details>

&nbsp;

### **Minecraft 1.16 and older (Java 8)**

Open terninal and type the following based on your distro
* Ubuntu/Debian derivatives: `sudo apt-get install openjdk-8-jre`
* Arch `sudo pacman -S jre8-openjdk`
* Fedora `sudo dnf install java-1.8.0-openjdk`
* OpenSUSE: `sudo zypper install java-1.8.0-openjdk`

Or you can manually download it

Eclipse Temurin: <https://adoptium.net/temurin/releases/?os=linux&arch=any&package=jre&version=8&mode=filter>

Scroll down until you see the single entry in the table!
<details>
<summary>Other Distributions</summary>

* Azul: <https://www.azul.com/downloads/?version=java-8-lts&os=linux&architecture=x86-64-bit&package=jre#zulu>
* Oracle: <https://www.oracle.com/java/technologies/downloads/#jdk8-linux>
</details>

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
