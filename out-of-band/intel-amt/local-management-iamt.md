---
description: Intel Active Management Technology
---

# Local Management (iAMT)

Intel Active Management Technology (Intel AMT) is a hardware-based technology for remote manageability of personal computers and servers. It allows IT administrators to remotely access devices and manage them regardless of the state of the operating system or power. Key capabilities provided by Intel AMT include remote power on/off, remote boot, hardware asset management, console access, and keyboard video mouse redirection. It utilizes its own embedded microcontroller and network interface card to enable out-of-band management that is isolated from the host system. Intel AMT is built into Intel chipsets and requires authentication and authorization for access, providing security for remote management. Overall, it is an essential technology for reducing hands-on IT support costs and improving efficiency in managing distributed PC and server fleets.

{% hint style="danger" %}
Note that the <mark style="color:blue;">**DeviceOn Server must be**</mark> <mark style="color:blue;">**on the same local network**</mark> as the edge device.
{% endhint %}

## Steps for Enabling

**Step 1:** To enable AMT, press **ESC** or **DEL** while the system is booting up, and navigate to **Advanced > AMT** Configuration.

<figure><img src="../../.gitbook/assets/image (97).png" alt=""><figcaption></figcaption></figure>

**Step 2:** From this screen, enable Intel AMT, save the settings, and then exit the BIOS setup.

<figure><img src="../../.gitbook/assets/image (98).png" alt=""><figcaption></figcaption></figure>

**Step 3:** Initiate a reboot of the system, and while the system is booting up, again press the **Ctrl and P keys.** Doing so will bring you to the Management Engine BIOS Extension (MEBx) Login screen, which will ask you for the default admin password (admin). It will then prompt you to set a new password (<mark style="color:blue;">must be at least eight characters long, contain at least one upper case character, one number, and one special character; it cannot contain any Unicode character</mark>). Once you have set the password, you can then reboot the system by pressing **Ctrl and P keys** once more. Afterward, select **MEBx Login** and log in as _**admin**_ with the password that you just set.

<figure><img src="../../.gitbook/assets/image (101).png" alt=""><figcaption></figcaption></figure>

**Step 4:** Select '<mark style="color:blue;">**Activate Network Access**</mark>' from the Intel AMT Configuration menu. This setting causes the ME to transition to the newly-provisioned state if all required settings have been configured. When MEBx displays **Update Network Settings** in the General Settings menu, press Enter. At the MEBx CAUTION prompt, press **Y**.

<figure><img src="../../.gitbook/assets/image (100).png" alt=""><figcaption></figcaption></figure>

## Accessing the Web Interface

**Step 1**: Power on an Intel AMT system that is in its operational phase.

**Step 2**: Invoke a web browser on a separate system (such as a management PC) that is on the same subnet as the Intel AMT system.

**Step 3**: Connect to the Intel AMT system using the IP address and port specified in the MEBx.

> By default, Intel® Active Management Technology (AMT) uses port 16992, and you can access it via <mark style="color:blue;">**`http://127.0.0.1:16992`**</mark>. However, if TLS (Transport Layer Security) is enabled on your AMT setup, you should use port 16993, accessed through <mark style="color:blue;">**`https://127.0.0.1:16993`**</mark>

{% hint style="warning" %}
Port 16992 has been discontinued for Intel® AMT communications. Only TLS (port 16993) is supported. This change was implemented with Intel® Core gen 12th and 13th. Intel® EMA software stopped supporting non-TLS connections.

[https://www.intel.com/content/www/us/en/support/articles/000089852/technologies/intel-active-management-technology-intel-amt.html](https://www.intel.com/content/www/us/en/support/articles/000089852/technologies/intel-active-management-technology-intel-amt.html)
{% endhint %}

The remote system makes a TCP connection to the Intel AMT system and accesses the top-level web page embedded within the ME

Enter your username and password. The default username is <mark style="color:blue;">**admin**</mark>, while the password is the one specified during ME setup. After login, the System Status screen appears

<figure><img src="../../.gitbook/assets/image (103).png" alt=""><figcaption></figcaption></figure>

{% hint style="danger" %}
Please note that if your device has multiple network ports, usually only one will be active. If the **IP** is not showing correctly, try the other network ports to find the active one.



For example, for the UNO-148 model, Network Port C must be used.

![](<../../.gitbook/assets/image (104).png>)
{% endhint %}

## Configure the DeviceOn Agent

Enable Intel AMT and configure the account credentials. The default account is "admin", and the password is what was specified during the Intel Management Engine (ME) setup. Reconnect to the DeviceOn server for the changes to take effect.

<figure><img src="../../.gitbook/assets/image (105).png" alt=""><figcaption></figcaption></figure>

If the configuration is correct, the DeviceOn Server will attempt to connect to the device's AMT. After a successful connection, the **Out-of-Band Intel AMT indicator light will turn on**, enabling power management capabilities.&#x20;

<figure><img src="../../.gitbook/assets/image (16).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (17).png" alt=""><figcaption></figcaption></figure>

Additionally, **Remote Desktop** will preferentially connect to the built-in VNC Server inside AMT.

<figure><img src="../../.gitbook/assets/image (18).png" alt=""><figcaption></figcaption></figure>
