# Agent Versions

## Operation Systems and Recommendations

* [**Windows 10/11 32-bit/64-bit**](https://eiot.blob.core.windows.net/deviceon/WISE-Agent%20for%20v5.0.zip)&#x20;
* [**Ubuntu 18.04, 20.04, 22.04 x64**](https://eiot.blob.core.windows.net/deviceon/WISE-Agent%20for%20v5.0.zip)&#x20;
* [**Ubuntu Core**](https://snapcraft.io/wise-deviceon-agent)&#x20;
* [**Ubuntu 18.04, 20.04 on Nvidia Jetson**](https://eiot.blob.core.windows.net/deviceon/WISE-Agent%20for%20v5.0.zip)&#x20;
* **CentOS 7.7, 8.2 x64**
* **Other Linux flavours (e.g. Yocto) on x86 or RISC (on a per project basis)**
* **Android on RISC (on a per project basis)**

_Assigned Ports for Device Communication_

| Name & Description         | Outbound Port                                   |
| -------------------------- | ----------------------------------------------- |
| MQTT, MQTTs Message Client | 1883, 8883                                      |
| Remote Desktop VNC Client  | <p>5501<br>8022 (v-1.4.45 and Server v-4.7)</p> |

**Hardware Minimum Requirements:**

* <mark style="color:blue;">**Intel® Celeron™ 1.10 GHz CPU and at least 2GB of RAM**</mark>
* <mark style="color:blue;">**500 MB root partition for the system**</mark>
* <mark style="color:blue;">**Advantech HW with respective SUSI driver 3.02/4.0 support is required for the HWM (Hardware Monitoring Management) feature to be available**</mark>

Advantech provides a device client that is used to communicate and exchange information between IoT (Internet of Things) devices and the DeviceOn cloud services, called **DeviceOn Agent**. DeviceOn Agent provides a rich set of user-friendly features that are intelligent, standardized and scalable.

* Standardization

> The communication protocol between client and cloud is based on the industry standard MQTT protocol. The IoT sensor data format is following the IPSO Alliance definition, implemented in JSON.

* Portability

> The whole framework is written in C language and follows the ANSI C Standard. C compilers are widely available for most platforms and allow easy porting to different architectures or operating systems.

* Scalability

> The DeviceOn Agent has a modular design and provides a plugin concept that allows flexible addition of new data sources or extra functionality.

DeviceOn Agent is support on different platforms running Windows 7 (or newer) or Ubuntu 16.04 x64 (or newer). Please contact us for others architectures (e.g. RISC) or operating systems (e.g. Yocto based Linux/Android).

## Agent Architecture

DeviceOn Agent includes two parts, one is the **Core Framework** and **Plugins**.

* **Core Framework** is the main library used to communicate with WISE-PaaS IoTHub or standard MQTT broker and include below components

1. Platform Profiler: describes the target platform (e.g., OS version, SN, Device name, MAC address)
2. Configuration: describes how to connect to MQTT broker (e.g., Credential URL, IoTKey, TLS/SSL settings)
3. Core Manager: integrates and manages the resources and keeps them alive.
4. Core Command: responsible for handling commands that interact with internal components (e.g., rename, update, get capability, auto report start/stop)
5. Plugin SDK: A plugin framework that makes plugin implement more easily.
6. Keep Alive: A component to detect the connection between DeviceOn Agent and DeviceOn Server.
7. Data Synchronization: kernel plugin that caches and restores data to ensure zero downtime.
8. Rule Engine: kernel plugin that supports the threshold rule check and then sends event or trigger actions
9. Plugin Loader: responsible for loading and managing plugins indicated in **module\_config.xml**



<figure><img src="../../.gitbook/assets/image (58).png" alt=""><figcaption></figcaption></figure>

* **The plugins** include IPC monitoring (Advantech Hardware, HDD/SSD, Networks, Process…etc.), control function (Backup/Recovery, Protection, Remote Desktop, Terminal…), and sensor protocol collection.

| SUSI Control           | Monitoring and Control Advantech Hardware Platform                                                            |
| ---------------------- | ------------------------------------------------------------------------------------------------------------- |
| HDD Monitoring         | Monitoring Hard Drives (HDD, SSD) Usage, Healthy and S.M.A.R.T Information, especially for Advantech SQFlash. |
| Network Monitoring     | Monitoring Network Interface Usage, Throughput…                                                               |
| Process Monitoring     | Monitoring System Process Status, CPU, Memory Usage.                                                          |
| Power Management       | Remote Control Power On, Off, Reboot, Sleep, Hibernate.                                                       |
| Backup/Recovery        | Remote Backup/Recovery System via Acronis                                                                     |
| Protection             | Remote System Protection via Trellix                                                                          |
| Remote Desktop         | Remote Desktop via VNC Viewer                                                                                 |
| Remote Terminal        | Remote Terminal Command                                                                                       |
| Remote Screenshot      | Remote Screenshot on Current Screen                                                                           |
| OTA (Over-the-Air)     | Remote Software, Firmware Update                                                                              |
| System Program         | Monitoring System Program Information                                                                         |
| Embedded Control       | Advanced Control (UWF, USB Lock, Keyboard Filter, …etc.) for Windows 10 Embedded, LTSC, LTSB                  |
| HDD Prediction         | Build-in Hard Drives (HDD, SSD) Failure Prediction Model                                                      |
| Modbus                 | Modbus Device Data Gathering                                                                                  |
| Service Plugin         | Bridge Southbound Device Service                                                                              |
| Local Provision Plugin | Similar to UPnP mechanism, provides device fast onboarding on local network.                                  |
