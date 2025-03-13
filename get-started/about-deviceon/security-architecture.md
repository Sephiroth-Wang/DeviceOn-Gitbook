# Security Architecture

<mark style="color:blue;">**System Security**</mark> is about not only installing and onboarding devices and networks securely but also managing their ongoing operations throughout their lifecycle and identifying and isolating any threats. Industries everywhere are digitizing, which is creating a multitude of new security requirements for the Internet of Things (IoT). End-to-end (E2E) security management will be essential to ensuring security and privacy in the IoT, while simultaneously building strong identities and maintaining trust. As the diversity of IoT services and the number of connected devices continue to increase, the threats to IoT systems are changing and growing even faster.

A comprehensive model of IoT device security, as shown in below structure, the comprehensive IoT module security in an IoT system has three main parts:

#### <mark style="color:blue;">**1. Device Security**</mark> <a href="#id-1_device_security_4" id="id-1_device_security_4"></a>

DeviceOn leverage Trellix Embedded Security software to prevents unauthorized changes and will lock a system down to a known application is an industry, that’s an industrial first solution to secure embedded devices.\
For disaster recovery, Acronis provides users a quick and easy-operated solution to protect data and recover the entire system even when OS crash, effectively reduces down-time cost and lowers the risk of data loss.

#### <mark style="color:blue;">**2. Secure Transport**</mark> <a href="#id-2_secure_transporty_9" id="id-2_secure_transporty_9"></a>

The server distributed SSL certificates to use TLS (v-1.3) as an encrypted and secure data transmission channel, and device default enable MQTT-SSL for communication.

* **Topics Isolation & Unique Device IoT Key**

Topics are specially handled in RabbitMQ. Topics are not public. Access control isolates an activated device to publishing/subscribing only to that device’s topics even though multiple devices will have subscriptions to identically named topics. A device is not allowed to subscribe/publish to another device’s topics.

Second, in IoT applications, command topics are used to control a device remotely and to acknowledge successful command executions. Unlike telemetry, command topics are not read-only. Commands are a back and forth workflow that can occur **between the cloud and devices**. Because commands are actionable messages, **isolate the MQTT topic for command messages from telemetry topics.**

* **Use x.509 Certificates to Authenticate Edge Device**

DeviceOn supports x.509 certificate authentication for use with a secure TLS/SSL connection. The x.509 edge device authentication **allows device to authenticate to servers with certificates rather than with a username and password.**

* **Use TPM + x.509 Certificates to Provide Higher Security**

The solution that we integrate on DeviceOn for Azure (Enterprise Edition), leverage Azure IoT Edge and TPM 2.0 to offer secure authentication and private key protected.

TPM, also known as [ISO/IEC 11889](https://www.iso.org/standard/66510.html), is a standard for securely generating and storing cryptographic keys. TPM also refers to a virtual or physical I/O device that interacts with modules that implement the standard. A TPM device can exist as discrete hardware, integrated hardware, a firmware-based module, or a software-based module.

#### <mark style="color:blue;">**3. Secure Cloud Service**</mark> <a href="#id-3_secure_cloud_service_28" id="id-3_secure_cloud_service_28"></a>

DeviceOn utilizes the **TPM module** for encryption and decryption, including database passwords and backup file data. It binds the encryption to the original device’s TPM, ensuring only that DeviceOn instance can run. This achieves a secured launch of the application and prevents the hard drive from being transferred to other devices.

By leveraging TPM hardware encryption, DeviceOn ties confidential data like credentials and backups specifically to the target device. The encryption keys exist only within that device’s TPM security chip. This prevents unauthorized access to sensitive information, even if the hard drive is removed.

Second, the cloud service components include Tomcat as a web server that provide an HTTPS protocol and backend APIs services, each connection between backend and database adopt SSL encryption, and enforce password policies. Second, for advanced attack, such as SQL injection, XXC, local and remote file vulnerabilities, the Nginx+Naxsi to achieve Web Application firewall (WAF) protection. All DeviceOn services pass through famous vulnerability tools to ensure security for your it IoT solutions, and the binary uses ProGuard code obfuscation protection. The APIs authentication not only uses JWT (JSON Web Tokens) to hide/encrypt sensitive data, but, integrate **LDAPs** & **Azure AD Domain Service** for secure.

![](https://docs.wise-paas.advantech.com/dataSource/resource/1611557937503425639.png)

## Role-based Access Control (RBAC)

DeviceOn supports three different user roles - “Root” (perpetual version only), “System Admin” and “Device Admin”. There is only one single “Root” account per system, which has the highest permission level and can create “System Admin” or “Device Admin” accounts. The intermediate user level “System Admin” can be used to create “Device Admin” accounts. “Device Admin” accounts have the lowest permission level.

**Two-factor authentication (2FA)** provides an additional layer of security when logging into websites or mobile applications. With 2FA enabled, users must authenticate in two steps. First, they enter their username and password. Then, they must provide a second form of authentication that only they possess, such as a code generated by an authenticator app or sent via SMS. 2FA helps protect accounts even if a password is compromised, because the second factor is still needed to log in. By requiring two pieces of information to gain access, 2FA makes it much harder for unauthorized users to log into your accounts.

## SSL Encryption

* _HTTPS on DeviceOn Web Server_

> The principal motivations for HTTPS are authentication of the accessed website, protection of the privacy and integrity of the exchanged data while in transit. It protects against man-in-the-middle attacks. The bidirectional encryption of communications between a client and server protects against eavesdropping and tampering of the communication.

* _SSL Connection on Database (PostgreSQL, MongoDB)_

> PostgreSQL and MongoDB have native support for using SSL connections to encrypt client/server communications for increased security.

* _Create Security Credentials on Database_

> Databases are by default protected by secure credentials and require explicit authentication for connections. This avoids accidentally deploying platforms with unprotected access.

* _Device Connectivity via MQTT SSL_

> RabbitMQ supports multiple protocols including MQTT, which the most popular IoT (Internet of Things) protocol. By default, SSL is used to encrypt all MQTT traffic for device connectivity.

* _Enforce Password Policies_

> While DeviceOn allows you to set some of your own passwords, please make sure those meet the minimum complexity requirements established by your specific organization.

## Security Scanner via Third-Party Tools

The DeviceOn server pass through below famous vulnerability tools to ensure security for your AIoT solutions. Furthermore, all the testing including anti-malware (**Trend Micro** and **Kaspersky**)

* _Web Application Assessment Report (Micro Focus)_

> [WebInspect](https://www.microfocus.com/zh-cn/products/webinspect-dynamic-analysis-dast/how-it-works) is an automated dynamic testing tool that mimics real-world hacking techniques and attacks, and provides comprehensive dynamic analysis of complex web applications and services.

* _OpenVAS (Open Vulnerability Assessment System)_

> [OpenVAS](http://www.openvas.org/) is a full-featured vulnerability scanner. Its capabilities include unauthenticated testing, authenticated testing, various high level and low-level Internet and industrial protocols, performance tuning for large-scale scans and a powerful internal programming language to implement any type of vulnerability test.

> The scanner is accompanied by a vulnerability tests feed with a long history and daily updates. This [Greenbone Community Feed](https://community.greenbone.net/t/about-greenbone-community-feed-gcf/) includes more than 50,000 vulnerability tests.

* _Nessus_

> [Nessus](https://www.tenable.com/products/nessus) is the de-facto industry standard vulnerability assessment solution for security practitioners. The latest intelligence, rapid updates, an easy-to-use interface.

1. Covers an industry-leading 47,000+ vulnerabilities
2. Unlimited scans at no extra cost
3. Compliant with PCI, HIPPA, GLBA, CIS, NIST, and more

* _OWASP ZAP_

> The [OWASP Zed Attack Proxy (ZAP)](https://owasp.org/www-project-zap/) is one of the world’s most popular free security tools and is actively maintained by hundreds of international volunteers\*. It can help you automatically find security vulnerabilities in your web applications while you are developing and testing your applications. It’s also a great tool for experienced pentesters to use for manual security testing.

* _Skipfish_

> [Skipfish](https://tools.kali.org/web-applications/skipfish) is an active web application security reconnaissance tool. It prepares an interactive sitemap for the targeted site by carrying out a recursive crawl and dictionary-based probes. The resulting map is then annotated with the output from a number of active (but hopefully non-disruptive) security checks. The final report generated by the tool is meant to serve as a foundation for professional web application security assessments.



1. High speed: pure C code, highly optimized HTTP handling, minimal CPU footprint – easily achieving 2000 requests per second with responsive targets.
2. Ease of use: heuristics to support a variety of quirky web frameworks and mixed-technology sites, with automatic learning capabilities, on-the-fly wordlist creation, and form autocompletion.
3. Cutting-edge security logic: high quality, low false positive, differential security checks, capable of spotting a range of subtle flaws, including blind injection vectors.

* _Nikto_

> [Nikto](https://tools.kali.org/information-gathering/nikto) is an Open Source (GPL) web server scanner which performs comprehensive tests against web servers for multiple items, including over 6700 potentially dangerous files/programs, checks for outdated versions of over 1250 servers, and version specific problems on over 270 servers. It also checks for server configuration items such as the presence of multiple index files, HTTP server options, and will attempt to identify installed web servers and software. Scan items and plugins are frequently updated and can be automatically updated.

* _W3af_

> [w3af](http://w3af.org/) is a **Web Application Attack and Audit Framework**. The project’s goal is to create a framework to help you secure your web applications by finding and exploiting all web application vulnerabilities.

* _Arachni_

> [Arachni](https://www.arachni-scanner.com/) is a fully featured web security scanning tool, it is based on ruby framework. It is an open source, modular and high performance tool. It comes with both command line interface as well as web based gui interface, it is highly versatile tool for security scanning purpose. It supports almost all of the popular web application such as HTML5, Java Script and AJAX etc, Additionally it is enables with multi user-multi platform collaboration.It allows you to generate reports in desired format (.txt, XML, HTML).

## Thrid-Party Vulnerability Fixed and Update

* OpenJRE, Eclipse Adoptium (v1.8.0422b06)
* Tomcat (v9.0.100)
* RabbitMQ (v3.13.7), Erlang 26.1.2
* PostgreSQL (v14.17)
* MongoDB (v6.0.20)
* Grafana (v9.5.21)
