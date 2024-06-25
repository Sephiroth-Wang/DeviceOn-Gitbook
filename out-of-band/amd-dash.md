---
description: Desktop and mobile Architecture for System Hardware
---

# AMD DASH

DASH (Desktop and mobile Architecture for System Hardware) is a client management standard released by the DMTF (Distributed Management Task Force) for secure out-of-band and remote management of desktops and mobile systems.

Client systems that support out-of-band management help IT administrators perform tasks independent of the power state of the machine or the state of the operating system. Examples of out-of-band management tasks include:

* Securely starting up a system remotely, even if it is currently powered off
* Viewing asset inventory information for a system that is powered off
* Retrieving health information about system components even if the OS is unavailable.

{% hint style="info" %}
DeviceOn currently integrates power management but does not include VNC capabilities. This omission is due to the proprietary nature of the VNC server, which is incompatible with VNC viewers.
{% endhint %}

{% hint style="danger" %}
Note that the <mark style="color:blue;">**DeviceOn Server must be**</mark> <mark style="color:blue;">**on the same local network**</mark> as the edge device.
{% endhint %}

## Steps for Enabling

In the following example, we will use the Advantech EBC-V001 for illustration purposes.

**Step 1**: Enable DASH from BIOS

To enable the Realtek DASH function, follow these steps:

1. Navigate to the **Advanced** settings.
2. Select **Realtek Dash Configuration**.
3. Set the **Realtek Dash function** to **Enable**

<figure><img src="../.gitbook/assets/image (142).png" alt=""><figcaption></figcaption></figure>

**Step 2**: Dash Setup Guide

To configure DASH, navigate through the following steps:

1. Click on **Advanced**.
2. Select **Realtek PCI GBE Family Controller**.

<figure><img src="../.gitbook/assets/image (155).png" alt=""><figcaption></figcaption></figure>

3. Choose **RealManage Setup**.

<figure><img src="../.gitbook/assets/image (156).png" alt=""><figcaption></figcaption></figure>

To modify the DASH configuration, you must enter your **username** and **password** if you have previously set up an account.&#x20;

<figure><img src="../.gitbook/assets/image (157).png" alt=""><figcaption></figcaption></figure>

For first-time users, you need to create an account follow these steps:

1. Go to **Setup and Configuration**
2. Select **Security Configuration**
3. Choose **Modify username and password**

<figure><img src="../.gitbook/assets/image (158).png" alt=""><figcaption></figcaption></figure>

4. After setting up your account and password, proceed to configure the network. Navigate to "**TCP/IP Configuration**" and enable DHCPv4. It is recommended to acquire the IP address from the DHCP server, similar to the in-band system.

<figure><img src="../.gitbook/assets/image (159).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (160).png" alt=""><figcaption></figcaption></figure>

5. Return to the **RealManage Setup** and ensure to **save** your configuration settings.

<figure><img src="../.gitbook/assets/image (161).png" alt=""><figcaption></figcaption></figure>

## Connect and Verify

Realtek offers a management tool known as the "**Realtek Management Console**." To connect and verify an AMD DASH device on your laptop, ensure both devices are on the same network.

<figure><img src="../.gitbook/assets/image (162).png" alt=""><figcaption></figcaption></figure>

To login to your DASH device, enter the **IP address**, along with the **username** and **password** you set up previously. Please ensure you connect through port **623** and verify that your device's firewall settings allow traffic on this port.&#x20;

<figure><img src="../.gitbook/assets/image (164).png" alt=""><figcaption></figcaption></figure>

After logging in, the manageability interface displays a submenu with monitoring information and functions, including **Computer Information**, **Hardware Details**, **Operating System Details**, **Software Inventory**, **Remote Control**, **Boot Control**, **Event Log**, **Account Management**, **Role Management**, **Network Settings**, **Alert Notifications**, and **KVM Redirection**.

## Configure the DeviceOn Agent

To apply the changes, enable AMD DASH, configure the account credentials, and then reconnect to the DeviceOn server.

<figure><img src="../.gitbook/assets/image (165).png" alt=""><figcaption></figcaption></figure>

If the configuration is correct, the DeviceOn Server will attempt to connect to the device's DASH. After a successful connection, the **Out-of-Band AMD DASH indicator light will turn on**, enabling power management capabilities.

<figure><img src="../.gitbook/assets/image (166).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (167).png" alt=""><figcaption></figcaption></figure>
