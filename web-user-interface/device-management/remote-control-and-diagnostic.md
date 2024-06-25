# Remote Control & Diagnostic

If you need to debug, diagnostic to your devices, actually, do not need go to field side. Through DeviceOn remote control to manage to reduce your operation effort. Basically, there are three functions (**Screenshot**, **Terminal** and **Remote Desktop**) for most devices.\


<figure><img src="https://i.imgur.com/I7uL416.png" alt=""><figcaption></figcaption></figure>

## Screenshot

Through the Screenshot to get device real-time screen, there is a limitation, _**your device must login to operation system**_, otherwise, cannot capture screen and shown “_**The OS of device is not logged in**_”. BTW, also support multiple screenshot, if your device connected multiple monitor.

<figure><img src="https://i.imgur.com/nU5YsMg.png" alt=""><figcaption></figcaption></figure>

## Terminal

To terminal support any command to your devices, for instance, realize your device IP, traceroute the network or copy/view file on the device.\


<figure><img src="https://i.imgur.com/7Uow1MK.png" alt=""><figcaption></figcaption></figure>

Both Windows and Linux supported.\


<figure><img src="https://i.imgur.com/s0ZyUG4.png" alt=""><figcaption></figcaption></figure>

## Remote Desktop

DeviceOn leverage VNC (Virtual Network Computing) technology to achieve remote desktop, to bridge different network between public and private. User do not need to install any program, App on their laptop or mobile devices. Through DeviceOn website to remote desktop to debug and diagnostic. _Please make sure your web client port (outbound) is allowed within (**6083**)_, and target device outbound port **8022**.

From server version **4.7** and above and DeviceOn Agent version with **1.4.45** later, all connections are _**encrypted end-to-end**_, and by default remote computers are protected by a random password and data encryption.

If your device supports **Intel AMT** and be configured without any problem, the remote desktop will try to connect the VNC server that through direct mode and the icon will appear in the top right corner).

<figure><img src="../../.gitbook/assets/image (72).png" alt=""><figcaption></figcaption></figure>

Second, if the Agent version higher than **1.4.45**, you could do the file transfer via drag-and-drop. The default storage path is ‘_**C:\Windows\Temp**_’.\


<figure><img src="https://i.imgur.com/RTuXPab.png" alt=""><figcaption></figcaption></figure>

## **Windows Lockdown Functions**

For others features depend on your device operation system and hardware. DeviceOn integrate Windows Lockdown features on 2019 LTSC (Long Time Service Channel) and 2016 LTSB (Long Time Service Branch) to provide advanced control, such as “**Block USB Drives**”, “**Keyboard Filter**”, “**Block Windows Notification**”, “**Block Touch**, **Gesture**” and “**UWF (Unified Write Filter)**”.

### Audio Volume

Remote adjust audio volume or mute/unmute which supports on Windows operating system.

<figure><img src="../../.gitbook/assets/image (73).png" alt=""><figcaption></figcaption></figure>

### USB Drives

Prevent threats from outside USB drives, not include keyboard, mouse.\


<figure><img src="https://i.imgur.com/jsvp5pd.png" alt=""><figcaption></figcaption></figure>

### Function Key

Disables Ctrl, Alt, and WinKey.\


<figure><img src="https://i.imgur.com/RD5iBwG.png" alt=""><figcaption></figcaption></figure>

### Windows Notification

Block application notification.\
![](https://i.imgur.com/t0CqUOp.png) ![](https://i.imgur.com/tVDxxqk.png)

### Touch Screen

Disable touch control\


<figure><img src="https://i.imgur.com/GK4scFb.png" alt=""><figcaption></figcaption></figure>

### UWF Protection

To protect your drives by intercepting and redirecting any writes to the drive (app installations, settings changes, saved data) to a virtual overlay. The virtual overlay is a temporary location that is usually cleared during a reboot or when a guest user logs off.

{% hint style="info" %}
**Benefits**:

1. Provides a clean experience for thin clients and workspaces that have frequent guests, like school, library or hotel computers. Guests can work, change settings, and install software. After the device reboots, the next guest receives a clean experience.
2. Increases security and reliability for kiosks, IoT-embedded devices, or other devices where new apps are not expected to be frequently added.
3. Can be used to reduce wear on solid-state drives and other write-sensitive media.
{% endhint %}

## Advantech Hardware Supported

For **backlight**, **brightness**, **GPIO** and **Watchdog** only support on Advantech hardware platform with SUSI driver, please download from [Advantech Support](https://support.advantech.com/) site.

### **SQFlash Self-Test & McAfee Virus Scan**

Part of SQ Flash have built-in McAfee Virus protection, you can update patterns and scan virus from DeviceOn.

<figure><img src="../../.gitbook/assets/image (74).png" alt=""><figcaption></figcaption></figure>

### **On-Screen Display (OSD, HDMI Interface)**

Adjust monitor (**brightness**, **color temperature**, **resolution**, …etc.), especially support on Advantech Industrial Display.\


<figure><img src="https://i.imgur.com/AYTi5Dr.png" alt=""><figcaption></figcaption></figure>

### **LVDS Backlight and Brightness**

Turn on/off LVDS backlight for power saving.\


<figure><img src="https://i.imgur.com/DNyZkLx.png" alt=""><figcaption></figcaption></figure>

### **Hardware Watchdog**

Hardware level watchdog to prevent BSoD (Blue Screen of Death) or system hang without any response. If happened, watchdog will restart your device automatically. There is an tool called [NotMyFault](https://docs.microsoft.com/en-us/sysinternals/downloads/notmyfault) that you can use to crash, hang, and cause kernel memory leaks on your Windows system.\


<figure><img src="https://i.imgur.com/nUvNHab.png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
**Benefits**:\
Avoid embarrassing moment, if BSoD on your Signage devices over the airport, department store and public area.
{% endhint %}

### **GPIO Control**

Adjust high, low for the hardware GPIO pin and direction (output or input).\


<figure><img src="https://i.imgur.com/DqC8AYN.png" alt=""><figcaption></figcaption></figure>

BTW, you could click **Edit** to rename GPIO00 for meaningful, for example factory light or fan.\


<figure><img src="https://i.imgur.com/bRkZefF.png" alt=""><figcaption></figcaption></figure>
