# Enable Passive Mode on FTP Server

{% hint style="info" %}
DeviceOn FTP default setting is active mode. However, FTP runs active mode may fail in cases where the server is behind a router or the server deplyed on Azure/AWS or other cloud’s virtual machine. And that will cause DeviceOn initialize failure. To solve this issue, you should change FTP server to passive mode.
{% endhint %}

## **Step 1**: Edit Configuration File

Open the **ftpd-typical.xml** on text editor tool that located in

```
\DeviceOn Path\ftp\res\conf\
```

Add the following XML attribute (data-connection) into listeners tag and give your **passive ports** range and **external DNS**.

```
<data-connection idle-timeout="60">  
  <passive ports="60001-60100" external-address="<YOUR_EXTERNAL_DNS>" address="0.0.0.0" />  
</data-connection>  
```

“**60001-60100**” means in passive mode, ftp client uses port 60001 to 60100 to transfer data. You could change it to any available ports range. “**YOUR\_EXTERNAL\_DNS**” means in passive mode, client’s destination domain name. You should replace it with real domain name which can be access from external side. After that, restart the service (**Apache FtpServer ftpd**) to apply setting.

![](https://i.imgur.com/lopIjzK.png)

## Step 2: Add inbound security rules

Add inbound security rules on your **network security group (ex, **<mark style="color:red;">**Azure Network Security Groups and Firewall Rules**</mark>**)**, make sure blow ports are available.

* **2121** (command port)
* **60001-60100** (Passive port)

## Step 3: Restart Service

Restart DeviceOn service, stop/start the “**Management Service**” via server tray icon.
