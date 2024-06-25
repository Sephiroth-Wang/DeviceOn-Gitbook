# User Interface

The newest DeviceOn Agent moves beyond just providing connectivity to enable more robust monitoring capabilities across managed endpoints. This version comes with an entirely redesigned web-based interface that reduces the agent’s footprint by approximately **50%** compared to previous versions. The web-based interface allows the agent to achieve true **cross-platform support**, capable of running on both x86 **Windows/Linux** platforms as well as **RISC-based** systems.

<figure><img src="../.gitbook/assets/image (35).png" alt=""><figcaption></figcaption></figure>

## Agent User Interface

The Agent interface has four main sections. The first page shows basic device information like OS version, CPU, memory and connectivity details. The second section is for real-time monitoring of the system and hardware. The third section is for system protection, primarily using Acronis and Trellix. Finally, the advanced settings section covers connectivity and other system configurations.

The Agent interface has four main sections. The first page shows basic device information like OS version, CPU, memory and connectivity details. The second section is for real-time monitoring of the system and hardware. The third section is for system protection, primarily using Acronis and Trellix. Finally, the advanced settings section covers connectivity and other system configurations.

![](https://hackmd.io/\_uploads/Hyx07YO4p.png)

The topmost section shows the device’s current status, including:

1. Connection Status: A green light indicates a successful connection to the DeviceOn Server. Otherwise, this area will appear grayed out.
2. Device Name
3.  Edit Device Name - Allows changing the device name\


    <figure><img src="https://hackmd.io/_uploads/HJ33Ht_Na.png" alt=""><figcaption></figcaption></figure>
4. Device version history
5. Unique Device ID
6. Language switcher - Toggle between multiple language options
7. Connect/disconnect from the DeviceOn Server

### **Information and Overview**

The Overview screen displays basic device information including OS version, CPU, memory, and connectivity details. For Advantech hardware with the SUSI driver installed, the model name and SUSI version number will automatically appear. Clicking the model name links to the product page for that hardware.

When connected to the DeviceOn Server, the top indicator light will show green. Additionally, the Overview will display the Server URL and a QR code. You can scan the QR code with a mobile device to start remote management.

![](https://hackmd.io/\_uploads/HJJXxYu4a.png)

### **Real-time Monitoring**

The Real-Time Monitoring section displays system-level information including CPU usage, memory utilization, network traffic, disk space, running processes, and more. For Advantech hardware, additional sensors (Voltage, GPIO, FAN and etc.) are enabled via the SUSI Driver.

The monitoring interface matches the DeviceOn Server, but connecting to the server is not required for local monitoring on the device itself. Some features like the Rule Engine and historical data storage are only available on the DeviceOn Server. For real-time monitoring locally on the device, no server connection is necessary.

![](https://hackmd.io/\_uploads/BJLZ\_FuN6.png)

### **System Shield**

If **Acronis** (for backup/recovery) or **Trellix (McAfee)** (for system protection) are not yet installed on the device, a download button will appear. Click the **download** button to get the installer and install the software locally.

![](https://hackmd.io/\_uploads/rkfJ75OEp.png)

{% tabs %}
{% tab title="Acronis Installation" %}
1.  After downloading the Acronis package and unzipping it, right-click on the **Administrator** and run AcronisInstaller.exe.\


    <figure><img src="https://hackmd.io/_uploads/H1DbJFFVa.png" alt=""><figcaption></figcaption></figure>
2.  Click **Agree** EULA to install.\


    <figure><img src="https://hackmd.io/_uploads/SyHK1FYEp.png" alt=""><figcaption></figcaption></figure>
3.  Enter the **Company Name** and **Serial Number** from the sticker on the Advantech hardware. Make sure to enter the **Company Name** and **Serial Numbe**r exactly as they appear on the sticker license. There should be a sticker located on the Advantech hardware that provides the necessary license details.\
    \


    <figure><img src="https://i.imgur.com/zRGaJEr.png" alt=""><figcaption></figcaption></figure>

    <figure><img src="https://hackmd.io/_uploads/SkHGfKtNa.png" alt=""><figcaption></figcaption></figure>
4.  By default, the system creates a hidden partition using half of the available disk space for backups. The size of this partition must be larger than the space currently used by the operating system and data.\


    <figure><img src="https://hackmd.io/_uploads/B1_0ltFEp.png" alt=""><figcaption></figcaption></figure>
5.  After completing the installation, the system will automatically reboot and create a hidden partition. You can view the **Acronis Secure Zone (ASZ)** partition in File Explorer or Disk Management on Windows. This partition is reserved for Acronis backups.\


    <figure><img src="https://hackmd.io/_uploads/HkVKqtKVa.png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Trellix Installation" %}
1.  Right-click on the installation file and run it as **Administrator**.\


    <figure><img src="https://hackmd.io/_uploads/H1D8N9d4a.png" alt=""><figcaption></figcaption></figure>
2.  Click **Agree** EULA to install.\


    <figure><img src="https://hackmd.io/_uploads/rylWHcuET.png" alt=""><figcaption></figcaption></figure>
3.  Enter the **Company Name** and **Serial Number** from the sticker on the Advantech hardware. Make sure to enter the **Company Name** and **Serial Numbe**r exactly as they appear on the sticker license. There should be a sticker located on the Advantech hardware that provides the necessary license details.\
    \


    <figure><img src="https://hackmd.io/_uploads/BJokDc_V6.png" alt=""><figcaption></figcaption></figure>

    <figure><img src="https://i.imgur.com/zRGaJEr.png" alt=""><figcaption></figcaption></figure>
4.  Click **Exit** to complete the installation. It is recommended to restart the system.\


    <figure><img src="https://hackmd.io/_uploads/H1BRD9O4a.png" alt=""><figcaption></figcaption></figure>
{% endtab %}
{% endtabs %}

#### System Backup & Recovery

Start backuping the system by clicking the **System Backup** button

<figure><img src="../.gitbook/assets/image (37).png" alt=""><figcaption></figcaption></figure>

Start recovering the system by clicking the **System Restore** button.

<figure><img src="../.gitbook/assets/image (38).png" alt=""><figcaption></figcaption></figure>

#### System Protection

Start protecting the system by clicking the **Protection** button.

<figure><img src="../.gitbook/assets/image (39).png" alt=""><figcaption></figcaption></figure>

### **Setting**

The Settings page contains three sections:

1. **Server Connection**: Enter the DeviceOn Server credentials here (**URL** and **IoT Ke**y). Selecting the **Trial Account** option will automatically connect to the DeviceOn Trial Site for evaluation purposes.
2. **VNC**: The DeviceOn Agent includes built-in UltraVNC for remote desktop access. You can specify a custom VNC server location if preferred. To disable remote desktop, select “**Disable KVM Connection**”.
3. **Intel AMT**: The Agent integrates Intel AMT (Intel Active Management Technology) for remote power cycling and remote desktop even if the OS crashes. This requires Intel Core i5/i7 hardware and the device must be on the same LAN as the Server. First enable and configure iAMT in the device BIOS. Then provide the iAMT account credentials here to enable remote management features.

<figure><img src="../.gitbook/assets/image (40).png" alt=""><figcaption></figcaption></figure>

### Logout and Change Passwords

The icon in the bottom left corner allows you to logout or change your password.

![](https://hackmd.io/\_uploads/BJF23KuVT.png)
