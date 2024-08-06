# Feature Highlight

## Device Connectivity & Monitoring

As Internet of Things deployments scale rapidly, securely onboarding the influx of devices to enable remote manageability is paramount. DeviceOn provides intelligent onboarding mechanisms to accommodate swift, robust IoT fleet integration.

The Zero-Touch provisioning module enables automatic device connectivity to DeviceOn post-power-on, sans manual configuration. This leverages DPS and TPM device capabilities for plug-and-play simplicity. Note Zero-Touch requires devices have native DPS/TPM support and network-level cloud access.

For devices lacking turnkey cloud connectivity, [**One-Time Configuration**](../../managed-devices/onboard-multiple-devices-at-once.md) facilitates standalone enrollment. Administrators manually configure one device with DeviceOn credentials. This gateway device in turn discovers and onboards peer devices by proxy. The proxy registration path allows DeviceOn compatibility even on private networks with no direct cloud access.

Post-integration, DeviceOn unlocks holistic health insights across registered devices. The system continuously collects fine-grained telemetry on critical performance vectors - [**disk**](../../web-user-interface/device-management/real-time-monitoring-and-rule-engine.md#hard-drive-disk-usage), [**CPU**](../../web-user-interface/device-management/real-time-monitoring-and-rule-engine.md#cpu-and-memory), [**memory**](../../web-user-interface/device-management/real-time-monitoring-and-rule-engine.md#cpu-and-memory), network. Admins can [**define thresholds**](../../web-user-interface/device-management/real-time-monitoring-and-rule-engine.md#rule-engine) for each vector to trigger realerts when deviations occur.

Additionally, the platform offers full extensibility to ingest data from proprietary sensors or non-standard IoT protocols. Custom device plugins can be developed to capture this data as part of the broader DeviceOn monitoring ecosystem.

In summary, DeviceOn solves the most pressing IoT integration obstacles - secure, expedient onboarding and multi-dimensional device insights - through both automated and customizable methods.

## Remote Diagnostics

DeviceOn enables robust remote troubleshooting and remediation across registered devices. Administrators gain multiple avenues to inspect device health and take corrective action from a central console.

* **Remote Access and Control (**[**Remote Desktop**](../../web-user-interface/device-management/remote-control-and-diagnostic.md#remote-desktop)**,** [**Screenshot**](../../web-user-interface/device-management/remote-control-and-diagnostic.md#screenshot)**,** [**Terminal**](../../web-user-interface/device-management/remote-control-and-diagnostic.md#terminal)**)**

The platform offers real-time remote desktop streaming via integrated KVM technology. This mirrors the device's native graphical interface for intuitive navigation. Alongside full control, admins can leverage selective monitoring options like screenshots and command line terminal access to quickly retrieve status or configuration data.

* [**App Store**](../../web-user-interface/app-management-ota.md#app-store-batch-deploy) **(Over the Air, OTA)**

DeviceOn coordinates seamless over-the-air firmware and software updates. The OTA framework integrates with external storage repositories like AWS S3, Azure Blob, FTP for scalable deployments. Agents can download bundles on a preset schedule to avoid bandwidth congestion. Rollback policies protect against failures, while custom scripting sets flexible pre/post update logic per device model.

* [**Power Management**](../../web-user-interface/device-management/device-list.md#power-management)

Administrators assign granular power schedules for groups or individual units based on daily, weekly or yearly cycles. For wider configurations, agents facilitate mass power control across complex network topologies.

* [**System Shield (System Protection)**](../../web-user-interface/device-management/device-list.md#system-protection-trellix-solidcore)

Embedded protections powered by Trellix monitor device activity to detect intrusions. App white-listing blocks unauthorized executable execution. All violations automatically alert admins for investigation.

* [**System Shield (Backup & Recovery**](../../web-user-interface/device-management/device-list.md#system-backup-and-recovery)**)**

Leveraging Acronis, DeviceOn enables one-click data backup with custom scheduling. One-click restore simplifies recovery from system failures or corrupt settings. This accelerates remediation while protecting against data loss.

* [**Hardware Monitoring**](../../web-user-interface/device-management/real-time-monitoring-and-rule-engine.md#hardware-level) **&** [**GPIO Control**](../../web-user-interface/device-management/remote-control-and-diagnostic.md#gpio-control)

DeviceOn gives you remote access to monitor and configure connected hardware components. Keep tabs on stats like GPU usage, fan speeds, display brightness and more. Set parameter thresholds so you're notified of issues before they cause failures. Take direct action by adjusting fan speeds, screen brightness, GPIO pins and other controls to tune device operation. This simplifies management without on-site visits.

* **Intuitive Ops Overview**

In general, the utmost goal of system integrators or IoT device operation managers is meeting service level KPIs without having to spend huge efforts or daily maintenance. Once hardware fails, it results in a serious increase in operation cost. DeviceOn provides rule-based management and implements HDD failure prediction. If a managed device shows any anomaly on a specific component or sensor, DeviceOn can send alert messages through **email** or **SMS,** or can optionally integrate with social media services such as **LINE**, **WeChat**. The DeviceOn overview shows overall status, upcoming schedule, top 5 potential risk devices as well as device location at a glance.

* **Flexible Notifications**

Find out about hardware faults or anomalies via **email**, **SMS** or social media bots. Integrate with workflow tools like **Slack**, **Teams ,** or **LINE**. Define rules so alerts reach the right people based on issue urgency.

In a nutshell, DeviceOn gives you simplified tools to head off problems before they interrupt operations or damage the bottom line.

## **Quick Data Integration**

DeviceOn delivers instant visibility into your fleet's performance right out of the box. Agents automatically feed device-generated data back to our management platform. Access this aggregated telemetry to visualize status or create custom Grafana dashboards with no coding needed.

Our wizard configures Grafana data sources using DeviceOn's JSON API in just a few clicks. Drag-and-drop to build monitoring panels that meet your unique needs. Customize at will as new metrics emerge. With data acquisition this simple, insights into device health are always within reach.

## **Effortless Group Administration**

Managing legions of distributed technology at scale can overwhelm even the most seasoned teams. DeviceOn removes these headaches with centralized, bulk control options from our portal.

Apply critical actions like power cycling, security policies, or system recovery to any subset of units in a single click. Need to disable screens during off hours? Our bulk brightness toggle has you covered. Automate and orchestrate routine upkeep so your team stays focused on strategic priorities.

Here's a sampling of one-click, bulk actions available:

* **Power Saving**
  * Power On/Off, Reboot, Sleep, Hibernate
  * \*Backlight On/Off
* **Security**
  * Protection On/Off
  * System Backup/Recovery
  * \*\*USB Lock/Unlock\
    Block USB drives and removable disks (_Not supported on Administrator user)_
* \*\*Keyboard Lock/Unlock\
  Block function key, such as **ALT**, **CTRL**, and **Windows key**.
* \*\*Touch Gesture Lock/Unlock (_supported with capacitive touch panel only)_
* \*\*Touch Lock/Unlock
* **System**
  * Screenshot
  * Audio Mute/Unmute
  * \*Watchdog Enable/Disable (_Default reset time is 60s)_\
    Reboots the system if it becomes unresponsive, to avoid hanging at **BSoD** (Blue Screen of Death) or similar situations
* \*\*Notification Block/Unblock

Disable windows notification from applications and other sources

* \*\*UWF Enable/Disable

Helps to protect your drives by intercepting and redirecting any writes to the drive (app installation, settings changes, and saved data) to a virtual overlay.

Above actions prefixed with ‘**\***’ require the respective Advantech SUSI Driver and actions prefixed with ‘**\*\***’ require following operating systems:

**Windows 10 Enterprise LTSC 2019 (LTSC)**

**Windows 10 Enterprise 2016 LTSB (LTSB)**

## Device Platform

* [**Windows 7 SP1/8/10/11 32-bit/64-bit**](https://eiot.blob.core.windows.net/deviceon/WISE-Agent%20for%20v5.0.zip)&#x20;
* [**Ubuntu 18.04, 20.04, 22.04 x64**](https://eiot.blob.core.windows.net/deviceon/WISE-Agent%20for%20v5.0.zip)&#x20;
* [**Ubuntu Core**](https://snapcraft.io/wise-deviceon-agent)&#x20;
* [**Ubuntu 18.04, 20.04 on Nvidia Jetson**](https://eiot.blob.core.windows.net/deviceon/WISE-Agent%20for%20v5.0.zip)&#x20;
* **CentOS 7.7, 8.2 x64**
* **Other Linux flavours (e.g. Yocto) on x86 or RISC (on a per project basis)**
* **Android on RISC (on a per project basis)**

## Cloud Deployment

* On-premise
* Private Cloud
* Public Cloud (Azure, AWS, WISE-PaaS/EnSaaS)
* Container

## Summary

Here is a summary for these feature highlights on different operation system and hardware requirement.

* **Standard Offering (Cloud Feature)**
  * **Authentication**
    * Detail:
      * Basic (base64) & JWT
      * LDAP & Azure AD Domain Service
      * Two-Factor Authentication, 2FA
    * Supported Platforms:&#x20;
      * Windows 7, 8, 10, 11
      * Ubuntu 18.04/20.04 x64
      * Ubuntu 18.04/20.04 on Nvidia Jetson
      * Linux on RISC (Yocto)
      * Android on RISC RSB-4710 (RK3399)
  * **Role-Based Access Control**
    * Detail:
      * Account & Role Management
      * Device & Device Group Management
    * Supported Platforms:&#x20;
      * Windows 7, 8, 10, 11
      * Ubuntu 18.04/20.04 x64
      * Ubuntu 18.04/20.04 on Nvidia Jetson
      * Linux on RISC (Yocto)
      * Android on RISC RSB-4710 (RK3399)
  * **Notification & Alert Service**
    * Detail:
      * Event Logs
      * Mail, SMS, LINE, WeChat, Telegram, Teams, Slack, Webhook
    * Supported Platforms:
      * Windows 7, 8, 10, 11
      * Ubuntu 18.04/20.04 x64
      * Ubuntu 18.04/20.04 on Nvidia Jetson
      * Linux on RISC (Yocto)
      * Android on RISC RSB-4710 (RK3399)
  * **Data Management**
    * Detail:
      * Device Real-time & Historical Data Monitoring
      * 1-Click to Data Visualization (Grafana)
    * Supported Platforms:
      * Windows 7, 8, 10, 11
      * Ubuntu 18.04/20.04 x64
      * Ubuntu 18.04/20.04 on Nvidia Jetson
      * Linux on RISC (Yocto)
      * Android on RISC RSB-4710 (RK3399)
  * **Operation Management**
    * Detail:
      * Batch Control & Statistical Analysis
      * Statics System Report
      * Task Scheduled
      * Device Map (Openstreet, Google, Baidu)
      * System Schedule Backup
    * Supported Platforms:
      * Windows 7, 8, 10, 11
      * Ubuntu 18.04/20.04 x64
      * Ubuntu 18.04/20.04 on Nvidia Jetson
      * Linux on RISC (Yocto)
      * Android on RISC RSB-4710 (RK3399)
* **Remote Control**
  * Device Zero-touch Onboarding
    * Supported Platforms:
      * Azure IoT Edge
  * Device Data Zero-Downtime
    * Supported Platforms:&#x20;
      * Windows 7, 8, 10, 11
      * Ubuntu 18.04/20.04 x64
      * Ubuntu 18.04/20.04 on Nvidia Jetson
      * Linux on RISC (Yocto)
  * Terminal
    * Supported Platforms:&#x20;
      * Windows 7, 8, 10, 11
      * Ubuntu 18.04/20.04 x64
      * Ubuntu 18.04/20.04 on Nvidia Jetson
      * Linux on RISC (Yocto)
  * Screenshot
    * Supported Platforms:
      * Windows 7, 8, 10, 11
      * Ubuntu 18.04/20.04 x64
      * Ubuntu 18.04/20.04 on Nvidia Jetson
      * Linux on RISC (Yocto)
      * Android on RISC RSB-4710 (RK3399)
  * Remote Desktop
    * Supported Platforms:
      * Windows 7, 8, 10, 11
      * Ubuntu 18.04/20.04 x64
      * Ubuntu 18.04/20.04 on Nvidia Jetson
      * Linux on RISC (Yocto)
      * Android on RISC RSB-4710 (RK3399)
  * Power Control - On/Off
    * Supported Platforms:
      * Windows 7, 8, 10, 11
      * Ubuntu 18.04/20.04 x64
      * Ubuntu 18.04/20.04 on Nvidia Jetson
  * Power Control - Reboot
    * Supported Platforms:
      * Windows 7, 8, 10, 11
      * Ubuntu 18.04/20.04 x64
      * Ubuntu 18.04/20.04 on Nvidia Jetson
      * Linux on RISC (Yocto)
      * Android on RISC RSB-4710 (RK3399)
  * Power Control - Sleep, Hibernate
    * Supported Platforms:
      * Windows 7, 8, 10, 11
      * Ubuntu 18.04/20.04 x64
  * System Backup/Recovery, Protection
    * Supported Platforms:
      * Windows 7, 8, 10, 11
  * Device Threshold Detection (Rule-based Engine)
    * Supported Platforms:
      * Windows 7, 8, 10, 11
      * Ubuntu 18.04/20.04 x64
      * Ubuntu 18.04/20.04 on Nvidia Jetson
      * Linux on RISC (Yocto)
  * App Store (OTA), Software, Firmware Provisioning
    * Supported Platforms:
      * Windows 7, 8, 10, 11
      * Ubuntu 18.04/20.04 x64
      * Ubuntu 18.04/20.04 on Nvidia Jetson
      * Linux on RISC (Yocto)
      * Android on RISC RSB-4710 (RK3399)
  * Process Monitoring & Control (Terminate, Restart, Launch)
    * Supported Platforms:
      * Windows 7, 8, 10, 11
      * Ubuntu 18.04/20.04 x64
      * Ubuntu 18.04/20.04 on Nvidia Jetson
      * Linux on RISC (Yocto)
  * Container Management (Start, Stop, Monitoring, Deploy)
    * Supported Platforms:
      * Windows 7, 8, 10, 11
      * Ubuntu 18.04/20.04 x64
      * Ubuntu 18.04/20.04 on Nvidia Jetson
      * Linux on RISC (Yocto)
  * Robot Operating System (ROS) Management
    * Supported Platforms:
      * Ubuntu 18.04/20.04 x64
  * Device Manager (Hardware Sentinel)
    * Supported Platforms:
      * Windows 7, 8, 10, 11
  * Audio Volume Control
    * Supported Platforms:
      * Windows 7, 8, 10, 11
      * Android on RISC RSB-4710 (RK3399)
  * Intel AMT Remote Control and Management
    * Supported Platforms:
      * Windows 7, 8, 10, 11
      * Ubuntu 18.04/20.04 x64
  * Intel IPMI Remote Control and Management
    * Supported Platforms:
      * Windows 7, 8, 10, 11
      * Ubuntu 18.04/20.04 x64
* **Advantech Hardware Support**
  * Hardware Watchdog Monitoring
    * Supported Platforms:
      * Windows 7, 8, 10, 11
      * Ubuntu 18.04/20.04 x64
      * Ubuntu 18.04/20.04 on Nvidia Jetson
      * Linux on RISC (Yocto)
      * Android on RISC RSB-4710 (RK3399)
  * Hardware GPIO Control & Customized (via SUSI Driver)
    * Supported Platforms:
      * Windows 7, 8, 10, 11
      * Ubuntu 18.04/20.04 x64
  * Brightness & Backlight Control
    * Supported Platforms:
      * Windows 7, 8, 10, 11
      * Ubuntu 18.04/20.04 x64
      * Android on RISC RSB-4710 (RK3399)
  * Hardware Sensor Monitoring (via SUSI Driver)
    * Supported Platforms:
      * Windows 7, 8, 10, 11
      * Ubuntu 18.04/20.04 x64
      * Linux on RISC (Yocto)
  * BIOS Update
    * Supported Platforms:
      * Windows 7, 8, 10, 11
      * Ubuntu 18.04/20.04 x64
  * BSP Update
    * Supported Platforms:
      * Linux on RISC (Yocto)
      * Android on RISC RSB-4710 (RK3399)
  * Advantech Industrial SQ Flash/RAM Remote Management & Monitoring
    * Supported Platforms:
      * Windows 7, 8, 10, 11
  * Advantech iBMC, Out-of-Band Remote Management (Cross-network)
    * Supported Platforms:
      * Windows 7, 8, 10, 11
  * Advantech Industrial Display, On-Screen Display (OSD) Management
    * Supported Platforms:
      * Windows 7, 8, 10, 11
* **Windows 10 Lockdown Features**
  * USB Drive Block
    * Supported Platforms:
      * Windows 10 LTSC, 11 LTSC Only
  * Keyboard Lock & Filter
    * Supported Platforms:
      * Windows 10 LTSC, 11 LTSC Only
  * Touch Screen & Gesture Lock
    * Supported Platforms:
      * Windows 10 LTSC, 11 LTSC Only
  * Windows Notification Block
    * Supported Platforms:
      * Windows 10 LTSC, 11 LTSC Only
  * UWF Protection
    * Supported Platforms:
      * Windows 10 LTSC, 11 LTSC Only
