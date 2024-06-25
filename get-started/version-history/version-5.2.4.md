# Version 5.2.4

## Security Topic

### IEC 62443 Compliance and the Cybersecurity Lifecycle

Advantech’s DeviceOn IoT solution is designed with insights from Lockheed Martin’s analysis of hacker attack patterns, including the stages of “**Reconnaissance**,” “**Weaponization**,” “**Delivery**,” “**Exploit**,” “**Installation**,” “**Command & Control**” and “**Action on Objectives**.” The development process of DeviceOn adheres to the operational procedures outlined in IEC 62443-4-1, which align with current product development practices and the Secure Software Development Life Cycle (SSDLC). These procedures are specifically tailored to meet the security development life cycle requirements and establish cybersecurity standards for the product.

The implementation includes various measures to mitigate potential security risks (IEC 62443 4-2 requirement) and enhance product safety.

1.  **IEC 62443-4-1 (Secure Development Lifecycle)**\
    The development process of DeviceOn adheres to the operational procedures outlined in IEC 62443-4-1, which align with current product development practices and the **Secure Software Development Life Cycle (SSDLC)**. These procedures are specifically tailored to meet the security development life cycle requirements and establish cybersecurity standards for the product.

    Throughout the design and development phase, DeviceOn diligently implemented a secure development policy in alignment with IEC 62443-4-1 standards. As part of this approach, comprehensive vulnerability scanning procedures were conducted to identify potential security weaknesses. [Various scanning tools such as **Nikto**, **Skipfish**, **w3af**, **OpenVAS**, **Nessus**, and **Sonarqube**](../about-deviceon/security-architecture.md#thrid-party-vulnerability-fixed-and-update) were employed to ensure thorough coverage.

    Furthermore, DeviceOn prioritized the assessment of third-party dependencies by subjecting them to rigorous testing. Tools such as **Trivy** were utilized to scrutinize these dependencies for any vulnerabilities or weaknesses that could compromise the system’s security.
2.  **IEC 62443-4-2 (Technical System Component Requirements)**\
    This standard specifies the technical **component requirements** (CR) for control systems. It relates to the fundamental requirements (FR) defined in IEC 62443-1-1 and defines the requirements to achieve security levels for control systems and components (SL-C). Previous versions of DeviceOn have already met most of the CRs and achieved the highest security level SL-4. In addition, the new version further enhances security for the following CRs:

    * [**Failed Login Lockout**](../../web-user-interface/system-setting.md#account-settings):

    ✔️ CR 1.11 Unsuccessful login attempts

    > Our DeviceOn provides comprehensive protection against brute force and dictionary attacks by implementing locks after a configurable number of unsuccessful login attempts. The system can be set to temporarily lock out users after a specified number of failed logins, with configure lockout durations to deter repeated guessing.

    <figure><img src="https://docs.wise-paas.advantech.com/dataSource/resource/1698045685819298672.png" alt=""><figcaption></figcaption></figure>

    * **TPM Support**:

    ✔️ CR 1.2 Software process and device identification and authentication\
    ✔️ CR 1.7 Strength of password-based authentication (SL2)\
    ✔️ CR 3.11 Physical tamper resistance and detection\
    ✔️ CR 3.12 Provisioning product supplier roots of trust\
    ✔️ CR 3.13 Provisioning asset owner roots of trust\
    ✔️ CR 7.3 Control system backup

    > DeviceOn utilizes the TPM module for encryption and decryption, including database passwords and backup file data. It binds the encryption to the original device’s TPM, ensuring only that DeviceOn instance can run. This achieves a secured launch of the application and prevents the hard drive from being transferred to other devices.

    > By leveraging TPM hardware encryption, DeviceOn ties confidential data like credentials and backups specifically to the target device. The encryption keys exist only within that device’s TPM security chip. This prevents unauthorized access to sensitive information, even if the hard drive is removed.

    * [**System Schedule Backup**](../../web-user-interface/system-setting.md#system-backup):

    ✔️ CR 7.4 Control system recovery and reconstitution

    > Indeed, our system provides comprehensive support for full configuration, data backup, and recovery. Additionally, each internal component offers independent installation and uninstallation capabilities. This modular approach enables users to customize and manage the system’s components according to their specific needs. With the ability to backup and recover configurations and data, our system ensures data integrity and facilitates seamless restoration in case of any disruptions or system failures.

    <figure><img src="https://docs.wise-paas.advantech.com/dataSource/resource/1698045858236654524.png" alt=""><figcaption></figcaption></figure>

    * **Device Decommissioning**:

    ✔️ CR 4.2 Information persistence

    > The system supports a device [**decommissioning** ](../../web-user-interface/device-management/device-list.md#actions-for-listed-devices)feature that allows for the complete erasure of all information, including device data, logs, and connection information. When a device is decommissioned, all its associated data and logs are securely wiped, ensuring that no sensitive information remains on the device. This feature helps to protect data privacy and maintain the system’s security by removing any trace of the decommissioned device from the system.

## Enhancement

### ROS Management

A graphical user interface to visualize active ROS nodes and inter-node communications via topics. This gives insight into the interactions between nodes in the ROS environment.

<figure><img src="https://docs.wise-paas.advantech.com/dataSource/resource/1698047350475635829.png" alt=""><figcaption></figcaption></figure>

Real-time logging of debug messages from each ROS node, aggregated and displayed through the DeviceOn interface. This allows admins to remotely monitor logs for troubleshooting.

<figure><img src="https://docs.wise-paas.advantech.com/dataSource/resource/1698047667439361354.png" alt=""><figcaption></figcaption></figure>

### Device Manager (Hardware Sentinel)

The Device Manager (Windows only) console enables live monitoring of connected peripherals and hardware, providing administrators high-fidelity tracking of USB-powered input devices like keyboards and mice, external USB storage drives, monitor, as well as any plug-and-play devices attached to managed systems. DeviceOn incorporates intelligent device recognition with continuous threat monitoring, include a virtual sentinel that stands guard and immediately triggers alert notifications if whitelist monitoring is enabled and new unauthorized devices are plugged in or known devices suddenly disconnected. This sophisticated device tracking and automated alert system gives administrators enhanced awareness and control to detect threats from unauthorized devices.

<figure><img src="https://docs.wise-paas.advantech.com/dataSource/resource/1698112368319936103.png" alt=""><figcaption></figcaption></figure>

### Brand-New DeviceOn Agent User Interface

The newest release of DeviceOn Agent moves beyond just providing connectivity to enable more robust monitoring capabilities across managed endpoints. This version comes with an entirely redesigned web-based interface that reduces the agent’s footprint by approximately 50% compared to previous versions. The web-based interface allows the agent to achieve true cross-platform support, capable of running on both x86 Windows/Linux platforms as well as RISC-based systems.

With this expanded compatibility, the agent can now provide extensive monitoring coverage across diverse endpoints, tracking vital performance metrics including CPU utilization, memory usage, disk activity, and active processes. The agent is also capable of monitoring Advantech hardware components and SQ Flash SSD installed on supported devices.

Moreover, this release integrates advanced local protection for endpoints through System Shield, which enables administrators to leverage Acronis backup and restore capabilities as well as Trellix system hardening directly on the endpoint itself. With the agent’s enhanced monitoring and System Shield integration, administrators gain greater visibility and control to secure and optimize their diverse endpoint environments.

<figure><img src="https://docs.wise-paas.advantech.com/dataSource/resource/1698134890978007307.gif" alt=""><figcaption></figcaption></figure>

### Great Improvement Performance (Device Capability)

Leveraging **RabbitMQ 3.12** and native MQTT, this release dramatically improves memory efficiency and reduces latency, boosting DeviceOn Server’s device connectivity capacity by up to 1 fold. When deployed standalone on an Azure VM using the **D4sV5** tier, a single DeviceOn Server instance can now easily support between <mark style="color:blue;">**9k**</mark> to <mark style="color:blue;">**10k**</mark> concurrent IPC device management.

## Third-Party Updates

* OpenJRE, Eclipse Adoptium (v1.8.392)
* Tomcat (v9.0.82)
* RabbitMQ (v3.12.7), Erlang 25
* PostgreSQL (v14.9)
* MongoDB (v5.0.19)
* Grafana (v9.5.13)

## Upgrade Version Path

Since MongoDB is the major database used by DeviceOn, we need to follow MongoDB's upgrade policy where users must successively upgrade between major releases. Since this version (v5.2.4) adopts MongoDB 5.0, if your current DeviceOn version is below 4.5.5, you need to first upgrade to [**version 5.1.2**](https://eiot.blob.core.windows.net/deviceon/Old%20Versions/Server/DeviceOn\_Server\_Setup\_5.1.2.exe) which uses MongoDB 4.4 before upgrading to this version.
