# Compliance

{% hint style="info" %}
#### `Security Objective: Compliance with IEC 62443 4-2 Standard`

The primary goal of implementing security measures is to <mark style="color:blue;">**`minimize risk`**</mark>. The IEC 62443 standard serves as a comprehensive guide for securing all aspects of product and field operations, covering both hardware and software components.

As an IoT platform, DeviceOn plays a crucial role in remotely managing devices distributed across various regions. It is imperative that we strive to achieve compliance with the IEC 62443-4-2 requirements, ensuring a secure and reliable service for our users.
{% endhint %}

## Enhancing Product Safety Through Comprehensive Security Measures

To safeguard our products and mitigate potential security risks, our implementation strategy incorporates a multi-faceted approach to enhance product safety. This involves:

* **Risk Assessment**: Employing risk assessment forms tailored for secure development ensures that vulnerabilities are identified early in the development process.
* **Vulnerability Verification**: Utilizing advanced automated tools for the detection of weaknesses helps in preemptively addressing potential security issues.
* **Managing Open-source Components**: Efficient inventory management of open-source components aids in mitigating risks associated with third-party software.
* **Cybersecurity Incident Management**: Our system tracks and effectively manages cybersecurity incidents to prevent future breaches.

**DeviceOn** is designed leveraging insights from Lockheed Martin’s analysis of hacker attack patterns—covering stages like Reconnaissance, **Weaponization**, **Delivery**, **Exploit**, **Installation**, **Command & Control**, and **Action** on **Objectives**. The development of **DeviceOn** strictly follows the operational procedures stated in IEC 62443-4-1, aligning with the Secure Software Development Life Cycle (SSDLC). This ensures that our development process not only meets but exceeds the security development life cycle requirements, establishing rigorous cybersecurity standards for our products.

## Main Security Features

### <mark style="color:blue;">System Integrity</mark>

#### Comprehensive Cybersecurity Solutions: From Edge to Cloud

Our cybersecurity approach encompasses every layer of your infrastructure, delivering robust security from the ground up. Our offerings include:

* **Edge Software Safeguards (**<mark style="color:blue;">**`Trellix`**</mark>** and **<mark style="color:blue;">**`Acronis`**</mark>**):** Enhance your edge computing software by integrating advanced security measures to protect against evolving cybersecurity threats.
* **Secure Communication Protocols (TLS/SSL):** Secure data communication within an Internet of Things (IoT) ecosystem is pivotal to maintaining the integrity and privacy of the data in transit. Implementing state-of-the-art protocols ensures that data exchanged between devices and servers remains confidential and tamper-proof.

#### Authenticity

To guarantee the integrity and verify the origin of software packages, it’s paramount to use digital signatures and checksums.  the digital signatures provide a secure way of confirming the software's origin and integrity. They use cryptographic techniques to generate a unique signature based on the software's contents. This signature is then attached to the software package.

#### Error Handling

Key components, including web services, are devised to manage data with utmost caution. This approach prevents the disclosure of too much information, which could leave the system open to attacks and exploitation by malicious entities.

### <mark style="color:blue;">Authentication & Authorization</mark>&#x20;

#### Multifactor Factor

Our communication system ensures robust security measures by implementing multi-factor authentication for all users. This multi-factor authentication approach significantly enhances the security posture of our communication system, reducing the risk of unauthorized access and mitigating the potential impact of compromised credentials.

#### Role-based Access

To safeguard against the danger of unauthorized privilege escalation, it is essential to segment access to devices and data based on specific permissions and roles. This strategic segmentation acts as a fundamental security measure, ensuring that each user operates within their designated authority level, minimizing the potential for security breaches.

### <mark style="color:blue;">Availability & Reliability</mark>

#### Ensuring High Availability in Critical Infrastructure

For domains where availability is paramount, such as factories or essential services, safeguarding against service interruptions is a key priority. Implementing flow control for both web and MQTT services is a strategic measure to prevent denial of service attacks. Additionally, enhancing system resilience involves:

* **Minimizing open ports**: Only maintain active the essential ports required for operation.
* **Embracing minimalism**: Adopt the principle of least functionality, enabling only those system features that are necessary to fulfill operational requirements.
* **Redundancy service**: Our system is configured with both primary and secondary servers. The primary server handles all operational tasks under normal conditions. The secondary server remains in standby mode, ready to take over instantly should the primary server fail.
* **System Backup**: In the event of a server compromise or failure, regular system backups serve as a critical recovery tool, enabling quick restoration to full functionality.

### <mark style="color:blue;">Data Sovereignty</mark>

DeviceOn offers support for both on-premise deployment as well as deployment on cloud platforms such as AWS, Azure and GCP. This ensures that you retain complete ownership and privacy of your data. Your data remains under your control, and unauthorized access is prevented. It's worth noting that if you choose to deploy on a public cloud, most cloud service providers already adhere to the **General Data Protection Regulation** **(GDPR)**, ensuring that your data is handled in compliance with stringent privacy and security standards. This provides an additional layer of assurance and eliminates concerns regarding the security and privacy of your data when leveraging public cloud infrastructure.

### <mark style="color:blue;">Accountability</mark>

#### Audit Logging and Log Management

Our system ensures accountability and traceability through detailed logging of all activities. These logs provide concrete evidence for who did what and when, incorporating:

* **Non-Repudiation:** Ensuring actions cannot be denied, adding an extra layer of security and accountability.
* **No Performance Trade-offs:** Logging processes are designed to run seamlessly, not affecting the system's inherent functionality.
* **Efficient Log Management:** Through log rotation policies, we maintain an optimal balance, keeping logs accessible without overwhelming storage.

## Advantech Certified Hardware: Value-Added Benefits

### <mark style="color:blue;">Security Boot</mark>

Our edge device is designed to boot only trusted firmware. At system start-up, DeviceOn executes a sequence of cryptographic algorithms to verify the authenticity and integrity of the software, ensuring it remains unaltered by unauthorized parties.

### <mark style="color:blue;">TPM Support</mark>

DeviceOn incorporates TPM (Trusted Platform Module) technology to securely encrypt database passwords and other credential data, enhancing overall data protection.

### <mark style="color:blue;">Unique Certificates</mark>

The device identification procedure utilizes a Trusted Platform Module (TPM) on the hardware level and is integrated within a Public Key Infrastructure (PKI) system. This architecture guarantees the creation of distinct and secure identities for each device.



