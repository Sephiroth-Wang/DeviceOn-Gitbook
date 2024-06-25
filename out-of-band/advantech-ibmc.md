---
description: Advantech Intelligent BMC Edge Intelligent Solution
---

# Advantech iBMC



Advantech’s intelligent board management controller (iBMC) is an embedded out-of-band management solution that simplifies the management of field systems and edge devices by allowing power management tasks (**`power on/off`**, **`force shutdown`**, and **`system reboot`**) to be conducted remotely, even in out-of-range conditions such as software failure or operating system (OS) crash. By enabling corrective action through remote out-of-band power management, iBMC technology eliminates the need for manual onsite power maintenance and reduces system downtime for industrial applications, such as continuous manufacturing and AI-based edge computing.

* Remote out-of-band power management
* Across OS, CPU platforms for multiple IPCs
* Default on/off in BIOS settings
* Powered by the ASIC hardware
* Integrated by software DeviceOn

The Out-of-Band (OOB) solution streamlines the process of device integration and management by leveraging cross-network functionality. Specifically, it establishes an active connection to the DeviceOn server via the MQTT protocol, eliminating the need for manual configuration. This innovative approach is facilitated by the in-band DeviceOn Agent, which autonomously communicates with the iBMC Agent, thereby securing a connection to the server with minimal user intervention.

This automated process significantly reduces the efforts and costs associated with deploying and provisioning devices on a large scale. By automating the communication and connection processes, organizations can swiftly integrate numerous devices into their networks without the extensive manual effort typically required. This efficiency is particularly beneficial for instances requiring mass provision of devices, offering a seamless, cost-effective solution for large-scale device management.

<figure><img src="../.gitbook/assets/image (168).png" alt=""><figcaption></figcaption></figure>

## Supported Hardware

To identify the hardware compatible with the iBMC solution, please visit the referenced website.

[https://www.advantech.com/en/products/ibmc-edge-intelligent-solution/sub\_6c53bcc8-1490-4e1e-a8d2-a56dc9a7f254](https://www.advantech.com/en/products/ibmc-edge-intelligent-solution/sub\_6c53bcc8-1490-4e1e-a8d2-a56dc9a7f254)

### Configurations?

If your hardware supports it and the BIOS is enabled, simply install the in-band DeviceOn Agent. It will automatically facilitate communication between the devices.&#x20;

Upon successful completion of the device onboarding process, the iBMC interface becomes actively engaged, symbolized through the illumination of the iBMC icon.&#x20;

<figure><img src="../.gitbook/assets/image (140).png" alt=""><figcaption></figcaption></figure>

Below are some of the pivotal actions that can be performed post-onboarding:

<figure><img src="../.gitbook/assets/image (141).png" alt=""><figcaption></figcaption></figure>

#### Power Management

Users have the autonomy to manage the power settings of the device, including but not limited to powering on or off the system remotely. This feature proves invaluable in managing systems distributed across various locations, offering flexibility and convenience in system administration.

#### Port 80 Status Monitoring

The interface provides real-time monitoring of the Port 80 status, which is crucial for troubleshooting and diagnosing boot-up issues. It offers insights into the post code sequences as the system initializes, helping in pinpointing potential problems early in the boot process.

#### Boot Sequence Configuration

Through the iBMC interface, users can specify the boot sequence for subsequent system startups. This capability allows for precise control over the boot process, ensuring that the system boots from the desired device or medium. Adjusting the boot sequence is essential when setting up systems for specific tasks or when troubleshooting boot-related issues.

#### Hardware-Level 1s Recovery (Powered by Apacer)

An innovative feature (**Coresnapshot 2**) powered by Apacer technology, the hardware-level 1s recovery, is an exceptional tool that enables users to restore their system to a predefined state within seconds. This functionality is crucial for minimizing downtime and ensuring that critical applications return online rapidly following system anomalies or failures.

{% embed url="https://www.youtube.com/watch?v=nptDgmCbgFY" %}
