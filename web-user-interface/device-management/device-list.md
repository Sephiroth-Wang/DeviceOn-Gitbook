# Device List

## Actions for Listed Devices

<figure><img src="../../.gitbook/assets/image (96).png" alt=""><figcaption></figcaption></figure>

1. Add Device

> Add devices that are not yet managed or onboard new devices.

2. Remove Device

> Remove management of the device from this account. The device still exists in the system, but this account no longer manages or owns it.

3. Delete Device (Decommissioning)

> Completely delete the device, removing all associated data and information from the database, including connection details.

4. Resync Device

> If the network connection is unstable, packets may sometimes be lost. This can lead to the app update status and device lock status becoming out of sync. You can resynchronize to get the latest device status again through Resync.

5. Export

> You can export the full list of devices currently managed under this account to a CSV file. This includes details such as device IDs, names, status, and more.

6. Searching for Device Owner

> If you are unsure which account a device currently belongs to, you can lookup the ownership by searching for the Device ID. The Device ID can be viewed on the device itself. This allows you to see which account is managing that device within the system.

## View Device

Click on device name or device details to get device information.

<figure><img src="https://i.imgur.com/TsPrt5j.png" alt=""><figcaption></figcaption></figure>

You could get the general information such as, device IP, version, MAC, Memory, BIOS, operation system and so on.

<figure><img src="https://i.imgur.com/oFkGkrU.png" alt=""><figcaption></figcaption></figure>

## Edit Device

Basically, you can modify the **device name**, **account** and **device group** on the page.

![](https://i.imgur.com/SJHZv5j.png)

### Intel Open AMT

DeviceOn supports **Open AMT (Open Active Management Technology Cloud Toolkit)** and **Device File Synchronization** after version **5.0** and DeviceOn Agent **v-1.4.48** or above.

If you have set up [**Open AMT service**](https://open-amt-cloud-toolkit.github.io/docs/2.6/) and configured it on the [**System Settings** **> Open AMT**](../system-setting.md#intel-open-amt), please bind the **GUID** of the corresponding device here, and you can perform **Out-of-Band (OOB)** management of the device through Open AMT.

{% hint style="info" %}
After your services deployed and device connect to Open AMT, you could get the GUID from the portal.
{% endhint %}

<figure><img src="https://i.imgur.com/MAgj9ZW.png" alt=""><figcaption></figcaption></figure>

{% embed url="https://www.youtube.com/watch?v=L-aVQBuHa3A" %}

### Device File Synchronization

The default folder for device file synchronization is **\DeviceOn Agent\filesync**. After configuring a remote repository under [**System Settings > Device File Synchronization**](device-list.md#device-file-synchronization), files in this local folder will automatically sync to the remote storage.

## Device System Log

Remotely collect Windows and Linux device logs for easier troubleshooting. Logs can be instantly downloaded through the built-in FTP server or alternatively configured servers set under [**System Settings > Device Logs**](../system-setting.md#device-logs).

{% hint style="warning" %}
The DeviceOn FTP server default is active mode. Active mode can fail if the server is behind a router or hosted on a cloud VM (Azure, AWS). This will cause DeviceOn initialization errors. To fix this, switch the FTP server to passive mode instead.

Please refer the FAQ to adjust FTP to passive mode.

[**How to Enable Passive Mode on FTP Server?**](https://hackmd.io/QKazc-aQSOqD3HIVshoMiQ#How-to-Enable-Passive-Mode-on-FTP-Server)
{% endhint %}

![](https://i.imgur.com/U6OwNSd.png)

![](https://i.imgur.com/hXP06Ve.png)

## Refuse Device Connection

{% hint style="danger" %}
Take the initiative to disconnect the device, and the device cannot automatically connect back to the server.
{% endhint %}

<figure><img src="../../.gitbook/assets/image (29).png" alt=""><figcaption></figcaption></figure>

## Power Management (In-band)

The power management supports **On/Off**, **Restart**, **Sleep** and **hibernate**, the actions depend on your device supported. These functions adopt software mechanism, and most of the industrial PC, personal laptop supported.

<figure><img src="../../.gitbook/assets/image (30).png" alt=""><figcaption></figcaption></figure>

The remote “**Power On**” is leverage **Wake-on-LAN** (WoL) protocol, that’s network standard allows a computer to be turned on. Enabling Wake-on-LAN is done in two steps, BIOS and Operating system Setup. Please reference the [site](https://www.lifewire.com/wake-on-lan-4149800) to configure your devices. Second, the WoL magic packet cannot cross different network, if your server is running on public cloud, it’s not on the same network as the devices, please ensure there is an alive device that connect to cloud, through the device to broadcast magic packet. On the DeviceOn portal, go to [**Device -> Provision -> PowerOn**](provision-and-configuration.md#power-on-wake-on-lan) to batch configure group devices on “**Agent Mode**”.

## System Shield

### System Protection (Trellix Solidcore)

The system protection is power-by Trellix whitelist protection mechanism to solidify device system. After enabling, 3rd execution file, bat, DLL cannot be launched.\


<figure><img src="https://i.imgur.com/qDlr5wz.png" alt=""><figcaption></figcaption></figure>

If the device is not installed, click the “**Install**”  to install Trellix, otherwise, click **Protect** or **Unprotect**. Device protection requires a rescan of the system files, which takes a while.

Go to [**Device -> Provision -> Trellix**](provision-and-configuration.md#system-protection-installation) for batch installation.

### System Backup and Recovery

The System Backup/Recovery is power-by Acronis to backup/recovery device runtime system partition. It’s will create a hidden partition called Acronis Secure Zone (ASZ) for backup image.\


<figure><img src="https://i.imgur.com/CMXVVDB.png" alt=""><figcaption></figcaption></figure>

If the device is not installed, click the “**Install**”  to install Acronis, otherwise, click **Backup** or **Recovey**. Device recovery requires reboot the system, which takes a while.

Go to [**Device -> Provision -> Acronis**](provision-and-configuration.md#system-backup-installation) for batch installation.

{% hint style="danger" %}
Important: The free space created must be larger than your current system used.
{% endhint %}

{% hint style="info" %}
If a DeviceOn license is already activated, Acronis/Trellix license prompts will not appear. Verify your DeviceOn server hardware has a valid sticker license. Enter the same **Company Name** and **Serial Number** from the sticker when prompted for Acronis/Trellix activation.\
![](https://i.imgur.com/otgHHOr.png)

<img src="https://i.imgur.com/zRGaJEr.png" alt="" data-size="original">
{% endhint %}

## Out-of-Band

<figure><img src="../../.gitbook/assets/image (133).png" alt="" width="190"><figcaption></figcaption></figure>

### [Intel AMT](../../out-of-band/intel-amt/)

Moreover, DeviceOn integrate Intel AMT (Intel Active Management Technology) for **power device up**, **reboot** and **hardware reset**. Please make sure you [enable the AMT function](../../out-of-band/intel-amt/local-management-iamt.md#steps-for-enabling) and [**configured on your DeviceOn Agent with AMT credential**](../../out-of-band/intel-amt/local-management-iamt.md#configure-the-deviceon-agent).

<figure><img src="../../.gitbook/assets/image (31).png" alt=""><figcaption></figcaption></figure>

{% embed url="https://www.youtube.com/watch?v=6fADiZIk3zc" %}

### [AMD DASH](../../out-of-band/amd-dash.md)

DeviceOn currently integrates power management but does not include VNC capabilities. This omission is due to the proprietary nature of the VNC server, which is incompatible with VNC viewers.

<figure><img src="../../.gitbook/assets/image (134).png" alt="" width="500"><figcaption></figcaption></figure>

For further configuration details on AMD DASH devices, please refer to the [LAB](../../out-of-band/amd-dash.md) documentation.

### [Advantech iBMC](device-list.md#advantech-ibmc)

Next advanced power option is Advantech developed a mini-Baseboard Management Controller named **iBMC** to provide out-of-band management. When the main system is abnormal or powered down, it can be powered on remotely and executed across networks, whether in public cloud or private.

#### Power Management

<figure><img src="../../.gitbook/assets/image (32).png" alt=""><figcaption></figcaption></figure>

#### Change Boot Order

Remotely change device boot order in BIOS settings. Configured boot order changes can be applied on next reboot, either via software restart or forced reboot.

<figure><img src="../../.gitbook/assets/image (33).png" alt=""><figcaption></figcaption></figure>

#### One-Key Backup/Recovery

Devices using an **Apacer Coresnapshot 2** hard drive can perform one-key backups and recovery when paired with compatible hardware and firmware.

<figure><img src="../../.gitbook/assets/image (34).png" alt=""><figcaption></figcaption></figure>

{% embed url="https://www.youtube.com/watch?v=nptDgmCbgFY" %}

### [Advantech Edge BMC](../../out-of-band/advantech-edgebmc.md)

Advantech's Edge BMC offers complete integration with DeviceOn, empowering users with full control over the current features of version 1.0. These features include:

1. **Sensor Monitoring (Out-of-Band)**
2. **BIOS Console Redirection**
3. **Power Management**

Used to power reset or shut down a device through a Edge BMC, rather than through the primary network interface of the device. This method allows administrators to manage and troubleshoot devices even if the primary network is down or the operating system is unresponsive, ensuring greater control and reliability in maintaining the device functionality.

## Agent Upgrade

For the DeviceOn Agent upgrade, if there is new version released by Advantech, it will check and show the icon  automatically.\


<figure><img src="https://i.imgur.com/I4CU0LN.png" alt=""><figcaption></figcaption></figure>

![](https://i.imgur.com/0kgHR2i.png)
