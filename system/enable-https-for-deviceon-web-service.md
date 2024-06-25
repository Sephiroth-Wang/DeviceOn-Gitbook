# Enable HTTPs for DeviceOn Web Service

{% hint style="info" %}
Generate Let’s Encrypt certificate using Certbot for DeviceOn.

* **Let’s Encrypt** is a new free, automated, and open source, Certificate Authority.
* **Certbot** is a console based certificate generation tool for Let’s Encrypt.\
  In this recipe, we will generate a Let’s Encypt certificate using Certbot. This certificate will then be deployed for use in the DeviceOn server.
{% endhint %}

## Dependencies:

* Port **443** for https needs to be open and available at time of executing certbot.
* Certbot needs root access while executing because only root is allowed to bind to any port below 1024.
* We will be using our own domain [myminio.com](http://myminio.com/) as an example in this recipe. Replace with your own domain under your setup.

## Steps to Configuration

* **Step 1**: Install Certbot

Install Certbot by following the documentation at [https://certbot.eff.org/](https://certbot.eff.org/)\
Since the DeviceOn Web service is running on Apache Tomcat, please select to “Apache” and “Windows” to downloads Certbot installer.

<figure><img src="https://i.imgur.com/MVBomfP.png" alt=""><figcaption></figcaption></figure>

Scrolling down the instruction, you may get the installer package on Step 4.\
[https://dl.eff.org/certbot-beta-installer-win32.exe](https://dl.eff.org/certbot-beta-installer-win32.exe)\


<figure><img src="https://i.imgur.com/tnWDj13.png" alt=""><figcaption></figcaption></figure>

Run the installer and follow the wizard. The installer will propose a default installation directory, C:\Program Files(x86), that can be customized.)\


<figure><img src="https://i.imgur.com/8hYmpV2.png" alt=""><figcaption></figcaption></figure>

* **Step 2**: Create the folder to authenticate

Create the folder named **acme-challenge** under **\<DeviceOn Folder>\server\portal.well-known**. If the folder “**.well-known**” is not exist, please create it manually (via CLI, for example: **mkdir**).\


<figure><img src="https://i.imgur.com/onGid7r.png" alt=""><figcaption></figcaption></figure>

* **Step 3**: Choose how you’d like to run Certbot\


Run the following command to create credential files and enter your website information. The domain name(s) should input yours and the webroot to **\DeviceOn Path\server\portal\\**

```bash
certbot.exe certonly --webroot
```

![](https://i.imgur.com/6P2m7Sg.png)

* **Step 4**: Install your certificate

You’ll need to install your new certificate in the configuration file or interface for your webserver. Certificates are located in **C:\Certbot\live\[certificate\_name]**, where **\[certificate\_name]** is the name of your certificate (usually the first domain if the **–cert-name** flag has not been used on the certonly command)\


<figure><img src="https://i.imgur.com/XDUf36K.png" alt=""><figcaption></figcaption></figure>

* **Step 5**: Install your certificate on DeviceOn Web Services
  * Open the server.xml on text editor tool that located in the **\DeviceOn Path\tomcat\conf\\**
  * Please <mark style="color:red;">**append**</mark> the new XML attribute '**Connector**' within the 'Service' tag, and provide the certification path (**lines 26 to 28**) that was generated during Step 4.

{% code lineNumbers="true" %}
```xml
<Connector port="443"   
    protocol="org.apache.coyote.http11.Http11AprProtocol"  
    connectionTimeout="20000"  
    useSendfile="false"  
    compression="on"  
    compressionMinSize="2048"  
    noCompressionUserAgents="gozilla, traviata"  
    compressableMimeType="text/html,text/xml,text/plain,text/css,text/javascript,application/javascript,application/xml,application/json"  
    redirectPort="8443"  
    maxThreads="150"  
    scheme="https"  
    secure="true"  
    SSLEnabled="true">    
    <UpgradeProtocol className="org.apache.coyote.http2.Http2Protocol"  
        overheadWindowUpdateThreshold="-1"  
        overheadDataThreshold="-1"  
        writeTimeout="-1"  
        streamWriteTimeout="-1"  
        streamReadTimeout="-1"  
        maxHeaderSize="8192"  
        maxConcurrentStreams="300"  
        readTimeout="-1"  
        compressibleMimeType="text/html,text/xml,text/plain,text/css,text/javascript,application/javascript,application/json"  
        compression="on" compressionMinSize="1024"/>    
    <SSLHostConfig>  
        <Certificate certificateKeyFile="C:\Certbot\live\<DNS>\privkey.pem"    
                     certificateFile="C:\Certbot\live\<DNS>\cert.pem"    
                     certificateChainFile="C:\Certbot\live\<DNS>\fullchain.pem"    
                     type="RSA" />    
    </SSLHostConfig>    
</Connector>
```
{% endcode %}

* **Step 6**: Restart DeviceOn web services (Tomcat\_IoT) to reload the configuration
*   **Step 7**: Replace the certificate files that in the websockify folder.

    ```bash
    xcopy "C:\Certbot\live\<DNS>\privkey.pem" "<INSTALLER_PATH>\server\portal\WEB-INF\classes\novnc\websockify\wise-paas.com.private.key" /Y
    ```

    ```bash
    xcopy "C:\Certbot\live\<DNS>\cert.pem" "<INSTALLER_PATH>\server\portal\WEB-INF\classes\novnc\websockify\wise-paas.crt" /Y
    ```
* **Step 8**: Enable to automatic renewal\


Create a batch file named **restartTomcat.bat** which content as below\


<figure><img src="https://hackmd.io/_uploads/Syf7xZdwn.png" alt=""><figcaption></figcaption></figure>

Copy the batch file into C:\Certbot\renewal-hooks\post\\

*   **Step 9 (Optional)**: Test automatic renewal, please run the following command

    ```bash
    certbot.exe renew –dry-run
    ```
*   **Step 10 (Optional)**: If you get all renewals succeeded, it means your configuration is correct.\


    <figure><img src="https://i.imgur.com/s5uWwiN.png" alt=""><figcaption></figcaption></figure>
* **Step 11**: <mark style="color:red;">Turn Windows firewall on inbound port</mark> <mark style="color:red;"></mark><mark style="color:red;">**443**</mark> <mark style="color:red;"></mark><mark style="color:red;">for your HTTPS, and make sure your network security rules allow</mark>.
* **Step 12**: Use the [**Server Configuration**](../user-interface-and-functions/server-standalone/server-management-tools.md#server-advanced-configuration) tool to update your web server configuration. For instance, if your previous web service URL was <mark style="background-color:orange;">**http://\<YOUR\_DNS>:8080**</mark>, change it to <mark style="background-color:orange;">**http**</mark><mark style="color:red;background-color:orange;">**s**</mark><mark style="background-color:orange;">**://\<YOUR\_DNS>**</mark>.&#x20;

<figure><img src="../.gitbook/assets/image (143).png" alt=""><figcaption></figcaption></figure>

After making the update, click '**Apply**' and then **restart** the <mark style="color:red;">**Tomcat service**</mark>.&#x20;

<figure><img src="../.gitbook/assets/image (144).png" alt=""><figcaption></figcaption></figure>

