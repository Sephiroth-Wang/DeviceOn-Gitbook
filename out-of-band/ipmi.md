---
description: Intelligent Platform Management Interface
---

# IPMI

IPMI (Intelligent Platform Management Interface) is a standardized computer system interface used by system administrators for out-of-band management of computer systems and monitoring of their operation. It is an open standard defining an abstracted interface to a computer system's motherboard sensors, control circuitry, and other embedded management functions.

The main benefits of IPMI include:

1. It allows administrators to manage systems independently of the operating system or processor, providing basic remote management capabilities.
2. It monitors system health aspects such as temperatures, voltages, fans, power supplies, etc.&#x20;
3. It provides console-level control capabilities like remote restart and power off.&#x20;
4. It logs system events, aiding in troubleshooting.&#x20;
5. It supports alerting capabilities to notify administrators of emergencies.

BMC chips enabling IPMI are typically only found in higher-end, server-grade systems. For example, Advantech's [**ARK-7000 Series**](https://www.advantech.com/en/products/ark-7000-series-extreme-performance-edge-servers/sub\_1-2jkloz) servers, [**FWA Series**](https://www.advantech.com/en/products/1u-intel-xeon-series-/sub\_bf4d0eac-80a3-4753-854d-732ad6b2e866) industrial servers, and [**ASMB industrial motherboards**](https://www.advantech.com/en/products/server-boards/sub\_serverboard) all support IPMI functionality. Details on their IPMI implementation can be found by reviewing the product specifications on the Advantech website. This chip-level integration allows for out-of-band management capabilities like remote monitoring and control of hardware components, independent of the operating system and main processors.

{% hint style="danger" %}
Note that the <mark style="color:blue;">**DeviceOn Server must be**</mark> <mark style="color:blue;">**on the same local network**</mark> as the edge device.
{% endhint %}

## Steps for Enabling

**Step 1**: Turn on the IPMI

To enable IPMI, press **ESC** or **DEL** during system boot-up to enter the BIOS setup utility. Then, navigate to the **Server Management** or **BMC Configuration** section. Using the `ASMB-586` as an example:&#x20;

<figure><img src="../.gitbook/assets/image (145).png" alt=""><figcaption></figcaption></figure>

**Step 2**: Setting Up the Address Source

For configuring the address source, it is recommended to adopt **`dynamic`** addressing assigned by the BIOS or BMC. Additionally, the ASMB-586 design has the **`LAN2`** port reserved and shared for IPMI network interface functionality.

<figure><img src="../.gitbook/assets/image (146).png" alt=""><figcaption></figcaption></figure>

## Accessing the Web Interface

**Step 1**: Logging into the Web Server

To access the web server, connect through the default HTTP port, which is **`80`**, use the default username and password, which are both "**`admin`**". Once logged in, you can change your password or username according to your preference.

<figure><img src="../.gitbook/assets/image (147).png" alt=""><figcaption></figcaption></figure>

**Step 2:** Accessing the Function and Verifying Configuration

Upon successful login, it indicates a correct configuration setup, allowing access to a wealth of features within the portal. These include comprehensive observation of sensors and **event logs**, along with **remote power management** capabilities.&#x20;

<figure><img src="../.gitbook/assets/image (148).png" alt=""><figcaption></figcaption></figure>

DeviceOn incorporates essential functionalities that facilitate device status monitoring and power management operations.

1. **Sensors** (“sensor” and “sdr” related commands) — practically using all the IPMI sensors as data source in DeviceOn.
2. **SEL** (System Event Log)
3. **Power on/off/graceful shutdown/cycle** as well as **reset** commands

## Configuring the DeviceOn Server

This guide provides concise steps to configure the DeviceOn Server. Follow the instructions below to ensure a successful setup.

**Step 1:** Enabling the IPMI User Interface

To enable the default IPMI's UI, follow these steps:

1. Navigate to [**Settings** > **System** > **System UI** > **System Menu**](../web-user-interface/system-setting.md#menu).
2. Enable the **IPMI item**.

Once enabled, the IPMI function will be accessible from the left menu bar.

<figure><img src="../.gitbook/assets/image (149).png" alt=""><figcaption></figcaption></figure>

**Step 2:** Configure the IP, Account, and Password in DeviceOn

To connect your device using IPMI, click the "**`+`**" button and enter the device's IP address, account username, and password.

{% hint style="warning" %}
Ensure that your DeviceOn server and the target IPMI device are on the same network.
{% endhint %}

<figure><img src="../.gitbook/assets/image (150).png" alt=""><figcaption></figcaption></figure>

If everything is functioning properly, you can select the "**`More`**" option to access the **`IPMI sensors`** and **`event log`**, as well as to conduct **`remote power management`**.

<figure><img src="../.gitbook/assets/image (151).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (152).png" alt=""><figcaption></figcaption></figure>
