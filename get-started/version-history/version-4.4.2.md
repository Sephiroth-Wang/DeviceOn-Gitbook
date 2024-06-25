# Version 4.4.2

## Security Feature

### <mark style="color:blue;">Topics Isolation & Unique Device IoT Key</mark>

Topics are specially handled in RabbitMQ. Topics are not public. Access control isolates an activated device to publishing/subscribing only to that device’s topics even though multiple devices will have subscriptions to identically named topics. A device is not allowed to subscribe/publish to another device’s topics.

Second, in IoT applications, command topics are used to control a device remotely and to acknowledge successful command executions. Unlike telemetry, command topics are not read-only. Commands are a back and forth workflow that can occur **between the cloud and devices**. Because commands are actionable messages, **isolate the MQTT topic for command messages from telemetry topics**.

### <mark style="color:blue;">Use x.509 Certificates to Authenticate Edge Device</mark> <a href="#font_colorblueuse_x509_certificates_to_authenticate_edge_devicefont_10" id="font_colorblueuse_x509_certificates_to_authenticate_edge_devicefont_10"></a>

DeviceOn supports x.509 certificate authentication for use with a secure TLS/SSL connection. The x.509 edge device authentication **allows device to authenticate to servers with certificates rather than with a username and password**.

### <mark style="color:blue;">Use TPM + x.509 Certificates to Provide Higher Security</mark> <a href="#font_colorblueuse_tpm__x509_certificates_to_provide_higher_securityfont_13" id="font_colorblueuse_tpm__x509_certificates_to_provide_higher_securityfont_13"></a>

The solution that we integrate on **DeviceOn for Azure (Enterprise Edition)**, leverage **Azure IoT Edge** and **TPM 2.0** to offer secure authentication and private key protected.

TPM, also known as [ISO/IEC 11889](https://www.iso.org/standard/66510.html), is a standard for securely generating and storing cryptographic keys. TPM also refers to a virtual or physical I/O device that interacts with modules that implement the standard. A TPM device can exist as discrete hardware, integrated hardware, a firmware-based module, or a software-based module.

<div align="center">

<img src="https://docs.wise-paas.advantech.com/dataSource/resource/1629256822008730488.png" alt="">

</div>

### <mark style="color:blue;">Securing Your Account with Two-Factor Authentication (2FA)</mark> <a href="#font_colorbluesecuring_your_account_with_twofactor_authentication_2fafont_21" id="font_colorbluesecuring_your_account_with_twofactor_authentication_2fafont_21"></a>

Two-factor authentication (2FA) is an extra layer of security used when logging into websites or apps. With 2FA, you have to log in with your username and password and provide another form of authentication that only you know or have access to.

If you prefer to use an authenticator app for two-step verification, here are a few common authenticator apps that can be found in your mobile device app store:

* **Google Authenticator**
* **Microsoft Authenticator**
* **Authy**
* **LastPass Authenticator**

<div align="center">

<img src="https://docs.wise-paas.advantech.com/dataSource/resource/1629354459442900934.png" alt="">

</div>

## Enhancement

### <mark style="color:blue;">Application Update History</mark>

Provide app deployment records to view which device groups, devices the app is deployed to, success and failure history records, including execution time and detailed logs.

<div align="center">

<img src="https://docs.wise-paas.advantech.com/dataSource/resource/1629257872239413467.png" alt="">

</div>

### <mark style="color:blue;">IAMT Library Update</mark> <a href="#font_colorblueiamt_library_updatefont_41" id="font_colorblueiamt_library_updatefont_41"></a>

Update [Intel® AMT High-Level API Module](https://software.intel.com/content/www/us/en/develop/download/intel-amt-high-level-api-sdk.html) to **15.0.2.1** to support new hardware platforms and chipsets.

### <mark style="color:blue;">Remote Desktop & Screenshot for Kiosk mode</mark> <a href="#font_colorblueremote_desktop__screenshot_for_kiosk_modefont_44" id="font_colorblueremote_desktop__screenshot_for_kiosk_modefont_44"></a>

For retail or digital signage scenarios, the current system users or devices are running in Kiosk mode. In order to allow administrators to operate remotely in this mode, we have improved Remote Desktop and Screenshot as well.

## Third-Party Updates

* OpenJRE (v1.8.0\_292-1)
* Tomcat (v9.0.50)
* RabbitMQ (v3.8.19), Erlang 24
* PostgreSQL (v10.17)
* MongoDB (v4.2.15)
* Grafana (v7.3.10)
