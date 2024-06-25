# Windows

## S**tep 1: Onboarding Your Device**

> Once your DeviceOn server installed, you could start to follow steps to onboarding your edge device.

1. &#x20;**Log in to the DeviceOn Cloud Service with Your Account and Password**

![](https://i.imgur.com/cs5FCGe.png)

2. **Download DeviceOn Agent and Connection Configuration (Agent.config)**

> At the first login, the “**Device Onboarding**” dialog will pop up automatically. Please click “Download” to get the latest version of DeviceOn AgentSetup.exe and the respective connection configuration. (Agent.config)

![](https://hackmd.io/\_uploads/r1BwW8u4a.png)

> Click “**Next**” to wait for connecting devices.

![](https://hackmd.io/\_uploads/SynqWIOEp.png)

3. **Set up Your Local Device**

> Copy those two files (**DeviceOn AgentSetup\_2.x.x.exe** and **Agent.config**) to the target device and launch “DeviceOn AgentSetup\_2.x.x.exe” as administrator.

![](https://hackmd.io/\_uploads/HymcxLu4a.png)

> Click “Next” to set up the DeviceOn Agent program.

![](https://hackmd.io/\_uploads/Byx348dNp.png)

> Select “**I Accept the terms in the License Agreement**” and click “**Next**”

![image](https://hackmd.io/\_uploads/SkhA4LO4a.png)

> When the “**DeviceOn AgentSetup\_2.x.x.exe**” program detects a cloud connection configuration file (Agent.config) in the same folder, “Quick Mode” as shown in this dialog will be available. For “**Quick Mode**”, the installation path is fixed to “C:\Program Files (x86)\Advantech\DeviceOn Agent”. If you would like to adjust the installation location, please select “**Advanced Mode**”.

{% tabs %}
{% tab title="Quick Mode" %}


![](https://hackmd.io/\_uploads/SyeErL\_E6.png)
{% endtab %}

{% tab title="Advanced Mode" %}
![](https://hackmd.io/\_uploads/HJk7MLdNT.png)
{% endtab %}
{% endtabs %}

> The DeviceOn Agent includes a web-based management interface. The default credentials are:
>
> * Username: admin
> * Password: admin

> You will be prompted to change the password after your first login. The web interface runs on port **8080** by default. This is the port you should use to access the management UI from a web browser. There is also a separate websocket port used internally for communication between plugins. You do not need to access this port directly.

![image](https://hackmd.io/\_uploads/r1\_6fUuVp.png)

> Set up the cloud connection configuration (**Credential URL** & **IoT Key**). This information can be retrieved from the DeviceOn web portal as shown in **Step 2**, and click “**Next**”.

* “**Zero-touch onboardin**g”: Only supported on Advantech platforms with SUSI Driver and pre-configuration on the provisioning server.
* “**Assign to User Account**”: Each account has its own connection IoTKey. If checked, the device will be assigned to this account automatically.
* “**Enable SSL**”: The communication between DeviceOn Agent and DeviceOn Cloud is MQTT. If checked (default setting), all the messages and content are SSL encrypted (<mark style="color:blue;">**MQTT SSL port: 8883**</mark>). Otherwise, port 1883 is used for MQTT without SSL.

![](https://hackmd.io/\_uploads/HyvorLONa.png)

> DeviceOn Agent supports remote desktop through built-in UltraVNC. You can manually specific the location of your own UltraVNC installation if preferred. If you do not want the remote desktop feature to be available, please select “Disable KVM Connection”.

![](https://hackmd.io/\_uploads/rJk1I8\_4p.png)

> DeviceOn Agent integrates Intel AMT (Intel Active Management Technology) for remote power management (Power Up, Down, Cycle and Reset) as well as remote desktop access, even in case the operating system has crashed. However, this feature requires hardware support (Intel Core i5, i7) and the target device needs to be on the same local network as the DeviceOn server. Please pre-configure iAMT, enable it in the device’s BIOS and provide the account and password information in this dialog if you would like to enable iAMT based remote control features.

![](https://hackmd.io/\_uploads/BJ1MLUOV6.png)

> Click “**Install**” to begin the installation.

![](https://hackmd.io/\_uploads/HkDBUIOVp.png)

> DeviceOn Agent requires the Microsoft Visual C++ Redistributable 2008, 2013, 2015 x86 packages, which will be downloaded from the Internet and set up during the installation process.&#x20;

{% hint style="info" %}
If you are in an environment with limited or no Internet access, please download the “[Agent Dependency Package](https://eiot.blob.core.windows.net/rmm-agent/AgentDependencySetup.exe)” through an Internet connected device and install this package first.
{% endhint %}

![](https://i.imgur.com/R1cJlI8.png)

## **Step 2: Launch the DeviceOn Agent**

> Click on the “**DeviceOn Agent**” link or the icon on the Windows Desktop to open the DeviceOn Agent user interface.

![](https://hackmd.io/\_uploads/HkE\_Tw\_Vp.png)

1. **Login to Agent Web Service**

![](https://hackmd.io/\_uploads/Sk7uCvuEp.png)

> The default username and password are both “**admin**”. Please change the password after logging in for the first time.

> If the status shows “**Disconnected**”, please make sure your network settings are configured correctly and that you have access to the DeviceOn server-side application, either located in a public cloud (Microsoft Azure, AWS) or on premise (standalone server version) depending on deployment scenario. Then, please click the “**Connect**” button to try to reconnect.

![image](https://hackmd.io/\_uploads/r1NXgu\_V6.png)

2. **Grouping Your Devices**

> Once the device connects, the DeviceOn user interface will move on to the device grouping page, where the device group for these devices can be selected.

![](https://i.imgur.com/JkXnKh7.png)

> There is a “**Default**” group that can be used, or other groups for this device can be created after checking “Advanced options”. Click “Confirm” to start device management.

![](https://i.imgur.com/5Jy0Dz9.png)

3. **Start Device Management**

> By default, two “**Real-time Actions**” are created for a group, one is “**Screenshot**” and the other one is “**Reboot**”. The overview page further shows the online status of registered.

![](https://i.imgur.com/30uFMjk.png)
