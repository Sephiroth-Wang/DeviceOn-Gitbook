# Version 4.5.5

## Security Feature

### <mark style="color:blue;">Device Backup & Recovery from External Storage (SMB/CIFS)</mark>

Support for remote device system backup to SMB/CIFS instead of a local drive, and recovery from SMB. For instance, a user could generate a golden operation system image, then restore to hundry of device in a factory, if needed. You also can leverage [Azure file to mount a SMB](https://docs.microsoft.com/en-us/azure/storage/files/storage-how-to-use-files-windows) on your remote system to achieve cloud backup.

### <mark style="color:blue;">Syslog Enabling</mark> <a href="#font_colorbluesyslog_enablingfont_7" id="font_colorbluesyslog_enablingfont_7"></a>

Syslog is a standard for message logging. It allows separation of the software that generates messages, the system that stores them, and the software that reports and analyzes them. Each message is labeled with a facility code, indicating the type of system generating the message, and is assigned a severity level. DeviceOn may use syslog for system management and security auditing as well as general informational, analysis, and debugging messages.\


<figure><img src="https://docs.wise-paas.advantech.com/dataSource/resource/1641957798496590015.png" alt=""><figcaption></figcaption></figure>

### <mark style="color:blue;">Securing Application Update through Digital Signature</mark> <a href="#font_colorbluesecuring_application_update_through_digital_signaturefont_11" id="font_colorbluesecuring_application_update_through_digital_signaturefont_11"></a>

The software release must traverse the internet and through many and sometimes unknown hands, and there are many potential attackers who might attempt to manipulate the software distribution process and alter the software release binaries for their own real-world gain. In order to avoid the software being tampered with and causing serious IoT losses, DeviceOn provides a digital signature method for the software, leveraged with **Azure Key Vault** to verify the correctness of the public key and avoid **Meet-in-the-middle attacks**.

### <mark style="color:blue;">Upgrade Apache Log4j2</mark> <a href="#font_colorblueupgrade_apache_log4j2font_15" id="font_colorblueupgrade_apache_log4j2font_15"></a>

Upgrade to the latest release of Apache Log4j and address false positive concerns with some vulnerability scanners. For previous and all version, DeviceOn do not used JNDI class and log4j-core, and also scanned/passed by official CISA scanner ([Log4j Scanner](https://github.com/cisagov/log4j-scanner)) and [Nessus](https://www.tenable.com/plugins/search?q=%22CVE-2021-4228%22\&sort=\&page=1).

## Enhancement

### <mark style="color:blue;">License Policy</mark>

Starting from **Version 4.5**, we have adjusted the license mechanism, DeviceOn provides two methods to activate the license, you can directly go to WISE-Marketplace to purchase or go to the Request Form to apply for a trial license. After you apply, the product team will review your request then send back the license file.

<figure><img src="https://docs.wise-paas.advantech.com/dataSource/resource/1644305480610570834.png" alt=""><figcaption></figcaption></figure>

* Managing DeviceOn Licenses: Activation, Expiration and Trials

{% embed url="https://www.youtube.com/watch?list=TLGG_qHQWIRKtMcyODExMjAyMw&v=tjZUchu0v2I" %}

* How to purchase DeviceOn license from WISE-Marketplace

{% embed url="https://www.youtube.com/watch?list=TLGGdGgI0EuF36AyODExMjAyMw&v=qrZ9nq5TsVc" %}

### <mark style="color:blue;">Webhook Service</mark>

In addition to the existing event notification via social media services (LINE, WeChat, Teams, Slack, Telegram), it also supports the integration of third-party APIs via Webhook. Such as **Microsoft Dynamics 365 Field Service**.

### <mark style="color:blue;">Data Export</mark> <a href="#font_colorbluedata_exportfont_34" id="font_colorbluedata_exportfont_34"></a>

The data export help to dump your sensor data as **CSV** or **JSON** format and upload to your cold storage, such as **Azure Blob**, **AWS S3** and **FTP** for advance data ingestion and learning through third-party. The generation time is every Sunday.

## Third-Party Updates

* OpenJRE (v1.8.0\_292-1)
* Tomcat (v9.0.50)
* RabbitMQ (v3.8.19), Erlang 24
* PostgreSQL (v10.19)
* MongoDB (v4.2.15)
* Grafana (v7.3.10)
