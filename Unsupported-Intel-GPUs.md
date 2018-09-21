If you use an older integrated Intel GPU (HD2000, HD3000), you will have to use an older version of Java.

Either one of those should work:
* https://files.multimc.org/downloads/jre-8u51-windows-x64.zip (64-bit)
* https://files.multimc.org/downloads/jre-8u51-windows-i586.zip (32-bit)

Download it, extract it into the MultiMC folder so it shows up like this:
![image](https://cloud.githubusercontent.com/assets/203326/24775694/31ee8d8a-1b1e-11e7-81d5-eff24add7de2.png)

Then set it up in MultiMc like this:
![image](https://cloud.githubusercontent.com/assets/203326/24775746/5c45fb22-1b1e-11e7-8615-e9ba6d667d7f.png)

Obviously only on Windows 10 :)

If you want the full background about this issue, see:
<details>

* https://github.com/LWJGL/lwjgl/issues/119
* https://github.com/MultiMC/MultiMC5/issues/1276
* (and many other)

I tried contacting Intel about it, they said they will not fix their drivers because the hardware is unsupported on Windows 10:

http://www.intel.com/content/www/us/en/support/graphics-drivers/000005526.html

... and Microsoft got an another person to boost their Windows 10 numbers, even though the hardware is not supported properly there.
</details>