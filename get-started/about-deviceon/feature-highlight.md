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

There is a summary for these feature highlights on different operation system and hardware requirement.



<table><thead><tr><th width="137"></th><th width="289">Feature Highlight</th><th>Windows 7, 8, 10, 11</th><th>Ubuntu 18.04/20.04 x64</th><th>Ubuntu 18.04/20.04 on Nvidia Jetson</th><th>Linux on RISC (Yocto)</th><th>Android on RISC RSB-4710 (RK3399)</th></tr></thead><tbody><tr><td><strong>Standard Offering (Cloud Feature)</strong></td><td><p><strong>Authentication</strong></p><ul><li>Basic (base64) &#x26; JWT</li><li>LDAP &#x26; Azure AD Domain Service</li><li>Two-Factor Authentication, 2FA</li></ul></td><td>●</td><td>●</td><td>●</td><td>●</td><td>●</td></tr><tr><td></td><td><p><strong>Role-Based Access Control</strong></p><ul><li>Account &#x26; Role Management</li><li>Device &#x26; Device Group Management</li></ul></td><td>●</td><td>●</td><td>●</td><td>●</td><td>●</td></tr><tr><td></td><td><p><strong>Notification &#x26; Alert Service</strong></p><ul><li>Event Logs</li><li>Mail, SMS, LINE, WeChat, Telegram, Teams, Slack, Webhook</li></ul></td><td>●</td><td>●</td><td>●</td><td>●</td><td>●</td></tr><tr><td></td><td><p><strong>Data Management</strong></p><ul><li>Device Real-time &#x26; Historical Data Monitoring</li><li>1-Click to Data Visualization (Grafana)</li></ul></td><td>●</td><td>●</td><td>●</td><td>●</td><td>●</td></tr><tr><td></td><td><p><strong>Operation Management</strong></p><ul><li>Batch Control &#x26; Statistical Analysis</li><li>Statics System Report</li><li>Task Scheduled</li><li>Device Map (Openstreet, Google, Baidu)</li><li>System Schedule Backup</li></ul></td><td>●</td><td>●</td><td>●</td><td>●</td><td>●</td></tr><tr><td><strong>Remote Control</strong></td><td>Device Zero-touch Onboarding</td><td></td><td>● Azure IoT Edge</td><td></td><td></td><td></td></tr><tr><td></td><td>Device Data Zero-Downtime</td><td>●</td><td>●</td><td>●</td><td>●</td><td></td></tr><tr><td></td><td>Terminal</td><td>●</td><td>●</td><td>●</td><td>●</td><td></td></tr><tr><td></td><td>Screenshot</td><td>●</td><td>●</td><td>●</td><td>●</td><td>●</td></tr><tr><td></td><td>Remote Desktop</td><td>●</td><td>●</td><td>●</td><td>●</td><td>●</td></tr><tr><td></td><td>Power Control (On/Off, Reboot, Sleep, Hibernate)</td><td>●</td><td>●</td><td>◐</td><td>◐</td><td>◐ Reboot Only</td></tr><tr><td></td><td>System Backup/Recovery, Protection</td><td>●</td><td></td><td></td><td></td><td></td></tr><tr><td></td><td>Device Threshold Detection (Rule-based Engine)</td><td>●</td><td>●</td><td>●</td><td>●</td><td></td></tr><tr><td></td><td>App Store (OTA), Software, Firmware Provisioning</td><td>●</td><td>●</td><td>●</td><td>●</td><td>◐</td></tr><tr><td></td><td>Process Monitoring &#x26; Control (Terminate, Restart, Launch)</td><td>●</td><td>●</td><td>●</td><td>●</td><td></td></tr><tr><td></td><td>Container Management (Start, Stop, Monitoring, Deploy)</td><td>●</td><td>●</td><td>●</td><td>●</td><td></td></tr><tr><td></td><td>Robot Operating System (ROS) Management</td><td></td><td>●</td><td></td><td></td><td></td></tr><tr><td></td><td>Device Manager (Hardware Sentinel)</td><td>●</td><td></td><td></td><td></td><td></td></tr><tr><td></td><td>Audio Volume Control</td><td>●</td><td></td><td></td><td></td><td>●</td></tr><tr><td></td><td>Intel AMT Remote Control and Management</td><td>●</td><td>●</td><td></td><td></td><td></td></tr><tr><td></td><td>Intel IPMI Remote Control and Management</td><td>●</td><td>●</td><td></td><td></td><td></td></tr><tr><td><strong>Advantech Hardware Support</strong></td><td>Hardware Watchdog Monitoring</td><td>●</td><td>◐</td><td></td><td></td><td>●</td></tr><tr><td></td><td>Hardware GPIO Control &#x26; Customized (via <strong>SUSI Driver</strong>)</td><td>●</td><td>●</td><td></td><td></td><td></td></tr><tr><td></td><td>Brightness &#x26; Backlight Control</td><td>●</td><td>●</td><td></td><td></td><td>●</td></tr><tr><td></td><td>Hardware Sensor Monitoring (via <strong>SUSI Driver</strong>)</td><td>●</td><td>●</td><td></td><td>◐</td><td></td></tr><tr><td></td><td>BIOS Update</td><td>●</td><td>●</td><td></td><td></td><td></td></tr><tr><td></td><td>BSP Update</td><td></td><td></td><td></td><td>●</td><td>●</td></tr><tr><td></td><td>Advantech Industrial SQ Flash/RAM Remote Management &#x26; Monitoring</td><td>●</td><td></td><td></td><td></td><td></td></tr><tr><td></td><td>Advantech iBMC, Out-of-Band Remote Management (Cross-network)</td><td>●</td><td></td><td></td><td></td><td></td></tr><tr><td></td><td>Advantech Industrial Display, On-Screen Display (OSD) Management</td><td>●</td><td></td><td></td><td></td><td></td></tr><tr><td><strong>Windows 10 Lockdown Features</strong></td><td>USB Drive Block</td><td>● Win10, 11 LTSC Only</td><td></td><td></td><td></td><td></td></tr><tr><td></td><td>Keyboard Lock &#x26; Filter</td><td>● Win10, 11 LTSC Only</td><td></td><td></td><td></td><td></td></tr><tr><td></td><td>Touch Screen &#x26; Gesture Lock</td><td>● Win10, 11 LTSC Only</td><td></td><td></td><td></td><td></td></tr><tr><td></td><td>Windows Notification Block</td><td>● Win10, 11 LTSC Only</td><td></td><td></td><td></td><td></td></tr><tr><td></td><td>UWF Protection</td><td>● Win10, 11 LTSC Only</td><td></td><td></td><td></td><td></td></tr></tbody></table>

\
