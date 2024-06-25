# Server Management Tools

## Start Menu

DeviceOn provides various widgets to assist server management, which can be found in Windows Start Menu.&#x20;

<figure><img src="../../.gitbook/assets/image (170).png" alt=""><figcaption></figcaption></figure>

Or can be found in installation path

```
C:\Program Files\Advantech\DeviceOn Server\Tools
```

## Service Management

After the DeviceOn standalone version has been installed, a “**Server Control**” icon should show up in the system tray.

![](https://i.imgur.com/LuRjHz9.png)

If it does not show up for some reason, please go to installation path and launch the program (**ServerControl.exe**) manually as shown here:

<pre><code><strong>C:\Program Files\Advantech\DeviceOn Server\Tools\Server Management
</strong></code></pre>

![](https://i.imgur.com/Viy1Urs.png)

Right-click the tray icon to open the status overview. A green light indicates the component is running normally. A red light means the corresponding service has stopped.

<figure><img src="../../.gitbook/assets/image (42).png" alt=""><figcaption></figcaption></figure>

* **Management Service**\
  The “Management” service includes the DeviceOn backend core function and consists of two Java processes (DeviceOn and Provisioning Worker) that handle messages and process OTA traffic between the client and server.
*   **Tomcat Service**\
    The DeviceOn web service uses Apache Tomcat to provide the user interface, APIs and WebSockets. For advanced configuration (SSL, connection pool, etc.), you may modify “server.xml” located in the installation folder.\


    <figure><img src="https://i.imgur.com/ucp94zI.png" alt=""><figcaption></figcaption></figure>
*   **PostgreSQL Service**\
    The relational database (PostgreSQL) is used to store account, device, map, permission data etc. A GUI tool called “**omnidb-server**” providing access to the PostgreSQL database comes with the PostgreSQL installation and is located in the installation folder as shown below. The default account is “**postgres**” and the password is the one you defined during the installation. We recommend you do not delete/edit any schema, table or data, since DeviceOn might stop to work if data is corrupt or missing.

    ![](https://i.imgur.com/qh1xOGP.png)

    The defaut port of omnidb-server is **8000**, and user/pwd is **admin**/**admin**.\


    ![](https://i.imgur.com/HpOHg0Y.png)

    <figure><img src="https://i.imgur.com/MfnD55u.png" alt=""><figcaption></figcaption></figure>
* **MongoDB Service**\
  To process sensor data from client devices, DeviceOn leverages MongoDB to provide better performance and compression rates than relational databases. Click “**Stop**” to stop the MongoDB service.
* **RabbitMQ Service**\
  RabbitMQ is one of the most popular open-source message brokers and is used as “IoT Hub” to exchange messages between the server and client devices.
* **Grafana Service**\
  Grafana is a popular framework that allows you to query, visualize and alert on data from various data sources. DeviceOn supports a simple JSON API that as can be used as data source in Grafana, effectively making all DeviceOn data available to Grafana.
* **FTP Service**\
  To remote deploy the application to edge device via OTA, DeviceOn build-in a FTP service (Apache FTP) as a default storage. The Apache FtpServer is a 100% pure Java FTP server. It’s designed to be a complete and portable FTP server engine solution based on currently available open protocols. FtpServer can be run standalone as a Windows service or Unix/Linux daemon or embedded into a Java application.

## Reset to Default

The DeviceOn server package includes a built-in restoration tool to revert your settings. You may need to use this if device configurations, data, apps, or system settings get changed without your knowledge. The tool will restore your server to its original post-installation state while retaining your current installation settings. All customizations made since installation will be overwritten.

```
C:\Program Files\Advantech\DeviceOn Server\Tools\Reset to Default
```

![](https://i.imgur.com/hKKxse6.png)

![](https://i.imgur.com/dovOMkO.png)

## Server Advanced Configuration

The DeviceOn Server IP Adjustment tool allows quick modifications when needed, without reinstalling the server. Some cases where you may need to update the IP:

* The IT network configuration changed the server IP
* The SSL certificate was updated

This tool can change the IP entered during initial installation to a new fixed IP or domain name. This allows edge devices to connect after network changes.

Additionally, the tool can:

* Modify the root account username suffix
* Enable automatic MongoDB data recycling to clear old data from capped collections

```
C:\Program Files\Advantech\DeviceOn Server\Tools\Server Configuration
```

<figure><img src="../../.gitbook/assets/image (44).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (43).png" alt=""><figcaption></figcaption></figure>

*   Web Server: Modify your IP/DNS Address.\
    **For Linux Server**:

    ```bash
    sudo sed -i "s/CURRENT_IP/NEW_IP/g" /opt/advantech/deviceon/etc/deviceon/Server_Config.xml
    sudo systemctl restart deviceon-portal.service
    ```

    **Example:**\


    <figure><img src="https://i.imgur.com/4WuGz8Y.png" alt=""><figcaption></figcaption></figure>
* Login Account: Modify a suffix to the Root account username
* MongoDB: Enable data recycling mechanism.
* WebRTC: Update STUN server for WebRTC, default adopt Google’s WebRTC.

## Server Diagnostic

The DeviceOn diagnostic tool helps technical staff troubleshoot server issues in the field. It checks the health of all services and collects relevant logs. After running the tool, a **log.zip** file is generated. Please send this to your DeviceOn support representative to assist with debugging any problems.

```
C:\Program Files\Advantech\DeviceOn Server\Tools\Server Diagnostic
```

![](https://i.imgur.com/g7JdIGh.png)

![](https://i.imgur.com/qKvOut4.png)

## Server Migration

The DeviceOn Server Migration tool, included in **v4.4.2+**, allows seamless transfer of your existing server installation to new hardware or cloud VMs (AWS/Azure). It migrates all device data, account information, configurations, etc.

![](https://i.imgur.com/2jnQkV5.png)

![](https://i.imgur.com/1SeRh9V.png)
