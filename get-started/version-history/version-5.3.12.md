# Version 5.3.12

## Out-of-Band Management

### AMD DASH

The AMD DASH (Desktop and mobile Architecture for System Hardware) technology enables IT administrators to manage and monitor AMD-based systems remotely. Leveraging out-of-band management capabilities, DASH allows for a range of tasks that are independent of the power state of the machine or the state of the operating system. This is particularly useful for various scenarios, including:

#### Securely Starting Up a System Remotely

Even if a system is currently powered off, administrators can securely start it up from a remote location. This ensures that critical updates or maintenance tasks can be performed at any time without the need for physic

#### Integrated AMD DASH Functions

With integrated AMD DASH out-of-band management functionality,  the administrators have enhanced control over AMD-based systems. Some of the key features provided by DASH include:

* **Remote Power Control:** Turning systems on, off, or rebooting them regardless of their current power state.
* **Hardware Monitoring:** Accessing hardware health status, including CPU temperature, fan speeds, and other critical metrics.

### Advantech Edge BMC

Advantech's Edge BMC offers complete integration with DeviceOn, empowering users with full control over the current features of version 1.0. These features include:

1. **Sensor Monitoring (Out-of-Band)**
2. **BIOS Console Redirection**
3. **Power Management**

Used to power reset or shut down a device through a Edge BMC, rather than through the primary network interface of the device. This method allows administrators to manage and troubleshoot devices even if the primary network is down or the operating system is unresponsive, ensuring greater control and reliability in maintaining the device functionality.

## Security and Access Policies <a href="#security-and-access-policies" id="security-and-access-policies"></a>

* Enabled user-configurable password validation rules, providing features for administrators to define and enforce custom password complexity requirements. This enhancement allows for greater security and flexibility by supporting various criteria such as minimum length, character types, and prohibited patterns.
* Implemented configurable login timeout settings, which help in improving security through the automatic logout of inactive sessions. This ensures that accounts remain protected by minimizing the window of opportunity for unauthorized access during idle periods.
* Introduced account deletion functionality, giving users the ability to permanently remove their accounts from the system. This feature respects user autonomy and privacy, allowing individuals to control their presence on the platform and ensuring that all their data is completely eradicated as per their request.

## Enhancement

### Major Updates

* **Intel AMT Power Management**: Enabled Intel Active Management Technology (AMT) support, allowing remote reset and power-on capabilities for Intel systems, including booting into BIOS.
* **Intel AMT Support**: Refactored Intel AMT's KVM function to support the latest ME version for SSL connection.
* **Agent Upgrade**: Upgraded DeviceOn Agent to a 64-bit version, improving performance and compatibility with modern systems.
* **GPU Management**: Implemented NVLink-based GPU monitoring and management capabilities, enabling efficient monitoring and control of NVIDIA GPUs.

## Dependency Upgrades <a href="#dependency-upgrades" id="dependency-upgrades"></a>

* Upgraded MongoDB from version 5.0.19 to 6.0.14, providing access to the latest features and bug fixes in the database management system.
* Upgraded RabbitMQ from version 3.12 to <mark style="color:red;">**3.13**</mark>, incorporating the latest improvements and security updates in the open-source message broker. <mark style="color:red;background-color:yellow;">This version only supports OpenSSL 3.x encryption. DeviceOn Agent versions lower than 1.4.50 will not connect successfully.</mark>
* Upgraded Vue.js from version 2 to 3, leveraging the latest features and performance improvements in the popular JavaScript framework.

### Third-Party Updates <a href="#third-party-updates" id="third-party-updates"></a>

* OpenJRE, Eclipse Adoptium (v1.8.0422b06)
* Tomcat (v9.0.100)
* RabbitMQ (v3.13.7), Erlang 26.1.2
* PostgreSQL (v14.17)
* MongoDB (v6.0.20)
* Grafana (v9.5.21)

## Upgrade Version Path <a href="#upgrade-version-path" id="upgrade-version-path"></a>

Since MongoDB is the major database used by DeviceOn, we need to follow MongoDB's upgrade policy where users must successively upgrade between major releases. Since this version (v5.3.2) adopts MongoDB 6.0, if your current DeviceOn version is below 5.2.4, you need to first upgrade to [**version 5.2.4**](https://eiot.blob.core.windows.net/deviceon/Old%20Versions/Server/DeviceOn_Server_Setup_5.2.4.exe) which uses MongoDB 5.0 before upgrading to this version.
