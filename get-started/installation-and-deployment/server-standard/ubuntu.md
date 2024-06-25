# Ubuntu

{% hint style="info" %}
If you are interested in DeviceOn and used to Linux platform, On-Premise, we also provide an installer for Ubuntu Linux (one of the most popular Linux distribution). This section will guide you how to install DeviceOn on Ubuntu Linux. Note here that:

* The DeviceOn Ubuntu Linux installer is named something like “**DeviceOn\_Server\_Ubuntu 20.04\_x64\_5.x.x.run**”. To acquire the installer and ensure having the latest version, please go to [resource page](../../../#deviceon-server).
* If you are running the installer with an account other than “<mark style="color:blue;">**root**</mark>”, you should use “<mark style="color:blue;">**sudo**</mark>” command to obtain higher privileges, or the installation may fail at any step.
{% endhint %}

## Steps to Installation

### Step 1: Open a terminal

> The installer runs in CLI (Command Line Interface) mode. As such, open a terminal preferable for you.

### **Step 2: Copy the installer to target host**

> Use the way you like to copy the installer to the target host.

### **Step 3: Set the installer as executable**

> In the terminal, run “sudo **chmod 0755 DeviceOn\_Server\_Ubuntu 20.04\_x64\_5.x.x.run**” so that the installer as an executable file under Ubuntu Linux.

```sh
sudo chmod 0755 DeviceOn_Server_Ubuntu-20.04_x64_5.x.x.run
```

### **Step 4: Running the installer**

> Change your working directory to where the installer is and run "**./DeviceOn\_Server\_Ubuntu 18.04\_x64\_5.x.x.run** ". You may need to run "**sudo ./DeviceOn\_Server\_Ubuntu 18.04\_x64\_5.x.x.run** " to acquire higher privileges if you were logged in as a normal user.

```sh
sudo ./DeviceOn_Server_Ubuntu-20.04_x64_5.x.x.run
```

### **Step 5: Answering some questions**

> This installer will guide you through installing DeviceOn onto your local machine. All you need to do throughout the installation process is answer some questions as prompted.

<figure><img src="../../../.gitbook/assets/image (45).png" alt=""><figcaption></figcaption></figure>

1. Please read the End-User License Agreement carefully. Press any key when you have finished reading and agree to the terms in order to continue with the installation.
2. Enter "<mark style="color:blue;">**yes**</mark>" to accept the license agreement.

<figure><img src="../../../.gitbook/assets/image (46).png" alt=""><figcaption></figcaption></figure>

3. Checking running mode and system dependencies...

<figure><img src="../../../.gitbook/assets/image (47).png" alt=""><figcaption></figcaption></figure>

4. Enter '<mark style="color:blue;">**y**</mark>', if you agree to install and use MongoDB.&#x20;

<figure><img src="../../../.gitbook/assets/image (48).png" alt=""><figcaption></figcaption></figure>

5. Installing required 3rd party packages, including OpenJRE, Erlang, MongoDB, PostgreSQL, Tomcat, Grafana, RabbitMQ, FTPD, OMIdb, MogoSH, etc.

<figure><img src="../../../.gitbook/assets/image (49).png" alt=""><figcaption></figcaption></figure>

6. DeviceOn license is tied to a network interface. The following lists all choose-able network interfaces information. To install DeviceOn, you have to determine which network interface to be tied to.

{% hint style="info" %}
It is strongly recommended to select a <mark style="color:red;">**physical network interface**</mark> instead of a virtual one. Choosing a physical interface avoids any potential issues DeviceOn may encounter in the future.
{% endhint %}

<figure><img src="../../../.gitbook/assets/image (51).png" alt=""><figcaption></figcaption></figure>

7. The password of user **postgres** to login PostgreSQL database. When you run into this step the question shows like above. Just input the password you would like to use to login PostgreSQL database for “**postgres**” account.

<figure><img src="../../../.gitbook/assets/image (52).png" alt=""><figcaption></figcaption></figure>

> When you run into this step the question shows like above. Just input the password you would like to use to login PostgreSQL database for “**postgres**” account.

8. The password of user “**wisepaas**” to login MongoDB database.

<figure><img src="../../../.gitbook/assets/image (53).png" alt=""><figcaption></figcaption></figure>

> When you run into this step the question shows like above. Just input the password you would like to use to login MongoDB database for “**wisepaas**” account.

9. If turn MongoDB capped functionality on or not.

<figure><img src="../../../.gitbook/assets/image (54).png" alt=""><figcaption></figcaption></figure>

> When you run into this step the question shows like above. Just input “**yes**” or “**no**” to enable or disable “capped” functionality. If you answer “yes”, a subsequent question followed to ask you “how much capped size, in MB, to be used? “. Just input the size, in MB, you want to use in “capped” functionality in MongoDB database.
>
>
>
> [Capped collections](https://docs.mongodb.com/manual/reference/glossary/#term-capped-collection) are fixed-size collections that support high-throughput operations that insert and retrieve documents based on insertion order. Capped collections work in a way similar to circular buffers: once a collection fills its allocated space, it makes room for new documents by overwriting the oldest documents in the collection.

{% hint style="warning" %}
The characteristic of capped cannot be disabled, if you enable the collection at first.
{% endhint %}

10. Enter '<mark style="color:blue;">**y**</mark>' to enable TPM to protect your IoT data and **encrypt**/**decrypt** credentials by TPM.

{% hint style="warning" %}
But pay attention to here that once you determine to introduce TPM into DeviceOn, it's not possible to disable in the future or DeviceOn will run into a big problem regarding encryption/decryption.
{% endhint %}

11. The valid IP or host name of the target host.

<figure><img src="../../../.gitbook/assets/image (55).png" alt=""><figcaption></figcaption></figure>

> When you run into this step the question shows like above. Just input the IP address of the target host. A hostname (even a FQDN) is also acceptable if you are sure that agents can connect to via the name you provide.

12. Enter the root email domain to use, type '<mark style="color:blue;">**y**</mark>' to use '<mark style="color:blue;">**root@advantech.com.tw**</mark>'. If you want to use your own domain, type '<mark style="color:blue;">**n**</mark>'.

<figure><img src="../../../.gitbook/assets/image (56).png" alt=""><figcaption></figcaption></figure>

13. The password of user “<mark style="color:blue;">**root@advantech.com.tw**</mark>” to login DeviceOn portal, and the rule should follow below guideline.

<figure><img src="../../../.gitbook/assets/image (57).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
#### Strong Password Rules:

_Minimum eight characters, at least one number, one lowercase letter, one uppercase letter, and one special character (Blank character, Backslash(\\), Double quotes(") are prohibited)_
{% endhint %}

When you run into this step the question shows like above. Just input the password you would like to use to login DeviceOn portal for “[**root@advantech.com.tw**](mailto:root@advantech.com.tw)” account.

Finally, a workable DeviceOn server should be there the target host. Open a browser and input **http://{IP-USED-IN-QUESTION-C}**, you should see the DeviceOn login page.



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

<figure><img src="../../../.gitbook/assets/image (15).png" alt=""><figcaption></figcaption></figure>

{% embed url="https://www.youtube.com/watch?v=tjZUchu0v2I" %}
