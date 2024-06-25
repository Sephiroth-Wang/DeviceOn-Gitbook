# Windows

## Steps to Installation

### Step 1: Install the DeviceOn

> Copy the installation file (**DeviceOn\_Server\_Setup\_4.7.x.exe**) to your target system and run it as administrator.

<figure><img src="https://i.imgur.com/JS30xJB.png" alt=""><figcaption></figcaption></figure>

> Click “**Next”** to start the installation process.

![](https://i.imgur.com/fvVIQgY.png)

> Select “**I Accept the terms in the License Agreement**” and click “**Next**”.

![](https://i.imgur.com/o36e7FW.png)

> Select the “**Installation Folder**” for DeviceOn Server and click “**Next**”

![](https://i.imgur.com/ncwtXPM.png)

> Enter “**Public IP**” or “**Domain Name**” for this physical/virtual machine and click “**Next**”. This information is required for “Edge Device” connectivity, please make sure your device is reachable under this IP or Domain Name.

![](https://i.imgur.com/wnqHZAb.png)

{% hint style="info" %}
You can start a Windows command prompt and type “**ipconfig**” to retrieve your IP address(es) on this physical/virtual machine.
{% endhint %}

![](https://i.imgur.com/molcVwv.png)

> You will need to configure the HTTP port number that is used for web browser-based access the DeviceOn management portal. The default port is **8080**, but you can select any other port as long as it does not conflict with any other application or service. Click “**Next**”.

![](https://i.imgur.com/w12nEKZ.png)

> Configure the password of the relational database (PostgreSQL) that DeviceOn uses to manage account, device, permission, and relation data. The default account name is “<mark style="color:blue;">**postgres**</mark>” and the password should follow below guideline.

{% hint style="info" %}
#### Strong Password Rules:

_Minimum eight characters, at least one number, one lowercase letter, one uppercase letter, and one special character (Blank character, Backslash(\\), Double quotes(") are prohibited)_
{% endhint %}

![](https://i.imgur.com/6Pt0v0D.png)

> Configure the password of the NoSQL database (MongoDB) that stores device sensor data. The default account and database is “<mark style="color:blue;">**wisepaas/WISE-PaaS**</mark>”. This password should also follow strong password rules as outlined above.

![](https://i.imgur.com/qhoJiFI.png)

> Select the database installation path and cache size of MongoDB and click “**Next**”. A larger cache size will result in better performance. For more information on this parameter, please referend to the [official documentation](https://docs.mongodb.com/manual/reference/configuration-options/#storage.wiredTiger.engineConfig.cacheSizeGB)

![](https://i.imgur.com/hK8BDO3.png)

> Enable **capped collections** for data recycling and set the size for each collections. Capped collections work in a way similar to circular buffers: once collection files its allocated spce, it make room for new documents by overwriting the oldest documents in the collection.

![](https://hackmd.io/\_uploads/Hka-Oa9L2.png)

{% hint style="warning" %}
The characteristic of capped cannot be disabled, if you enable the collection at first.
{% endhint %}

> Configure the password of the root account (dummy name “root@advantech.com.tw”) and click “Next”. This root account has the highest permission level and is used to log in to the DeviceOn web service and create other user accounts.

![](https://i.imgur.com/o7Yclnf.png)

> Set up the HTTP service port for Grafana dashboard. The default user name and password is admin/admin. You will be able to modify this at the first login.

![](https://i.imgur.com/lGqr8Ds.png)

> Set up FTP service port for application (App Store), device log storage.

![](https://hackmd.io/\_uploads/SkkN365U2.png)

> DeviceOn license is tied to network interface. The above lists all choose-able network cards information. To install DeviceOn, you have to determine which network card to be tied to. Choosing a <mark style="color:blue;">**connected and physical interface**</mark> over a virtual one is highly recommended to prevent potential issue that DeviceOn may encounter in the future.

![](https://hackmd.io/\_uploads/rJS5na9Ih.png)

> For devices with a TPM chip, TPM data encryption can be enabled to restrict DeviceOn Server execution solely to the same hardware, thus ensuring data security.

![](https://hackmd.io/\_uploads/rk7yaCFNT.png)

> Click “**Install**” to begin the installation.

![](https://i.imgur.com/4JYbOH6.png)

> Click the “Finish” to exit the program.

![](https://i.imgur.com/KsodnpN.png)

### Step 2: Launch DeviceOn Web Service

> Two shortcuts will be generated on the desktop - one is for the DeviceOn web portal and the other one is for the Grafana dashboard.

![](https://i.imgur.com/cy2s5hE.png)

> Click the “<mark style="color:blue;">**DeviceOn Server**</mark>” shortcut in order to launch a browser and to start device operation and management. It is recommended to use <mark style="color:blue;">**Chrome**</mark> for the best user experience.

![](https://i.imgur.com/9pPMIQ4.png)

## Activate License

### **Step 1**: Accept the EULA&#x20;

> Please read over and consent to the license agreements found below.

* [x] I accept this End User License Agreement
* [x] I accept that DeviceOn will send your user/system information and activated license data to Advantech to better understand possible application scenarios and improve your user experience.

<figure><img src="../../../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

### **Step 2**: Login to DeviceOn and Apply License

> Sign into DeviceOn with the account credentials you set up previously.

<figure><img src="../../../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

> Upon your first login, a notice will open asking you to start a free trial or obtain a paid license through product activation. Activating a license is a prerequisite to handle your IoT devices in the system.

<figure><img src="../../../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

> There are two license activation options: directly purchase from the **WISE-Marketplace (method 1)** or apply for a free trial (90-Day) via the **Request Form (method 2)**. Both require the **License Request Code**, which contains device information details like the **MAC address**. Please copy or download this code to use for either activation method.

<figure><img src="../../../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

#### Method 1:&#x20;

> If you already have a [WISE-Marketplace](https://wise-paas.advantech.com/en-us/marketplace/product/advantech.wise-paas-deviceon-iot-device-management-app/pricing-details) account created by Sales, go directly there to buy a DeviceOn license.&#x20;

<figure><img src="../../../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

> After purchasing, in the upper right go to the My Licenses page. Locate the inactive license, paste in your license request code to activate it, and download the license file.

{% embed url="https://www.youtube.com/watch?v=qrZ9nq5TsVc" %}

#### Method 2:&#x20;

> Use the [request form](https://wesstorage.blob.core.windows.net/cloudservice/deviceon/license.html) to input your personal information. Be sure to correctly fill out both your <mark style="color:blue;">**email**</mark> and the copied <mark style="color:blue;">**License Request Code**</mark>. Once you've verified the details are all accurate, submit the form. The trial license will be sent to the email you provide as soon as it is prepared.

<figure><img src="../../../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>

> When the audit process is done, expect an email from us containing the attached license file.

<figure><img src="../../../.gitbook/assets/image (13).png" alt=""><figcaption></figcaption></figure>

### **Step 3**: Import License File

> Locate the license attached in the email and activate it with the "**Activate**" button.

<figure><img src="../../../.gitbook/assets/image (14).png" alt=""><figcaption></figcaption></figure>

{% embed url="https://www.youtube.com/watch?v=tjZUchu0v2I" %}
