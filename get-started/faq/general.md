# General

<details>

<summary>How can I receive DeviceOn product updates and news?</summary>

You are welcome to visit the following pages for more information and experience on DeviceOn.

* [DeviceOn Product Page](https://wise-paas.advantech.com/en-us/marketplace/product/advantech.wise-paas-deviceon-iot-device-management-app)
* [News & Solution Package](https://campaign.advantech.online/en/DeviceOn/index.html)

</details>

<details>

<summary>How can I download the DeviceOn server and agent software?</summary>

Please try to get the installer package from below download link.

* [DeviceOn Server](https://eiot.blob.core.windows.net/deviceon/DeviceOn\_Server.zip) (Windows & Ubuntu)
* [DeviceOn Agent](https://eiot.blob.core.windows.net/deviceon/WISE-Agent.zip) (Windows & Ubuntu)

</details>

<details>

<summary>How can I monitor device hardware status?</summary>

The device hardware information includes FAN Speed, Voltage, Watchdog and brightness. Before monitoring this information on DeviceOn, please make sure your device is Advantech hardware and with SUSI driver support. Recommend to download SUSI driver from [Advantech Support](https://support.advantech.com/) site for your hardware platform first. Click [**here**](https://www.dropbox.com/s/4p46gtzpm57u4jr/SUSI4\_Std.exe?dl=0) get the latest driver version.

</details>

<details>

<summary>How can I purchase a license?</summary>

Please contact Advantech sales and join to WISE-Marketplace member to purchase license for DeviceOn.

[https://www.youtube.com/watch?v=qrZ9nq5TsVc](https://www.youtube.com/watch?v=qrZ9nq5TsVc)

</details>

<details>

<summary>What is the maximum number of devices that DeviceOn can manage?</summary>

It depends on your server configuration. Taking the Azure DeviceOn VM specification, as an example, the instance D2sV5 is able to manage **1000**pcs devices. If you need to manage more than 1000 devices, please contact us for advanced solution and architecture.

</details>

<details>

<summary>How can I deploy DeviceOn on Azure?</summary>

It is really simple that just login Azure Marketplace and search for **DeviceOn**, then follow the steps to create a virtual machine. Here is a [**Quick Start Guide**](../installation-and-deployment/server-standard/azure-marketplace.md) to deploy through Azure Marketplace.

</details>

<details>

<summary>Which operating systems support the DeviceOn agent?</summary>

Please refer to the section about [**DeviceOn Agent Supported Operating Systems**](../about-deviceon/agent-versions.md#operation-systems-and-recommendations) for details.

</details>

<details>

<summary>Can DeviceOn execute bulk operations on devices remotely?</summary>

Yes, group the devices for different attributes and set the task for each group, bulk operation can be finished. Please refer to the below sections.

* [App Management](../../web-user-interface/app-management-ota.md)
* [Container Management](../../web-user-interface/container-management.md)
* [Task Management](../../web-user-interface/device-management/task-management-batch-control.md)

</details>

<details>

<summary><mark style="background-color:red;">Does DeviceOn provide an SDK?</mark></summary>

DeviceOn offers easy customization with a complete [REST API](https://docs.wise-paas.advantech.com/en/Guides\_and\_API\_References/ApplicationServices/1564727799415968385/1609292788571761649/v1.0.0) for core management on the server side, and an [SDK](https://docs.wise-paas.advantech.com/en/Guides\_and\_API\_References/ApplicationServices/1564727799415968385/1609292785115116876/v1.0.0) on the device side that enables the development of custom plugins.

</details>

<details>

<summary>How to Upgrade Software, Firmware via DeviceOn?</summary>

DeviceOn has OTA (Over The Air) function to remote provisioning and updates on firmware, driver, and software at the scale. Please refer the [App Management, OTA](../../web-user-interface/app-management-ota.md) for details

</details>

<details>

<summary>How can I obtain DeviceOn support?</summary>

Please contact below window to get further information.

mail to: [DeviceOn.Support@advantech.com](mailto:DeviceOn.Support@advantech.com)

</details>

## Which Azure VM tier and size should I select, and what are the cost estimates?

It is recommended that users select **D2sV5** (2Cores 8G RAM) to meet most cases, you may refer below scenarios that we verified. The list price of VM, storage is based on [Azure calculator](https://azure.microsoft.com/en-us/pricing/calculator/) and the data center in **Southeast Asia** (Singapore)

{% hint style="info" %}
January 22, 2022, based on v-4.5.1 of DeviceOn Server.
{% endhint %}

{% hint style="info" %}
Case I, Standard IPC Device Management (Hardware, Network, Hard Disk, System), **25Tags/min**
{% endhint %}

| **Azure VM Tier (WinSrv 2019)**  | **Device** **Number** | **Storage** **Required/mo** | **Storage Tier (HDD) Recommended (Monthly Retention)** | **Price Estimation WinSrv 2016 + Storage (USD)/mo** | **Price Estimation Ubuntu 18.04 + Storage (USD)/mo** |
| -------------------------------- | --------------------- | --------------------------- | ------------------------------------------------------ | --------------------------------------------------- | ---------------------------------------------------- |
| D2sV5 (2 Cores 8G) ($158.46/mo)  | 10                    | 1.09G                       | S6 (64G), $3.06/mo                                     | **$161.52**                                         | **$90.66**                                           |
|                                  | 100                   | 8.22G                       | S6 (64G), $3.06/mo                                     | **$161.52**                                         | **$90.66**                                           |
|                                  | 500                   | 39.9G                       | S10 (128G), $5.94/mo                                   | **$164.4**                                          | **$93.54**                                           |
|                                  | 1,000                 | 79.5G                       | S10 (128G), $5.94/mo                                   | **$164.4**                                          | **$93.54**                                           |
|                                  | 3,800                 | 302.1G                      | S20 (512G), $21.81/mo                                  | **$180.27**                                         | **$109.41**                                          |
| D4sV5 (4 Cores 16G) ($316.87/mo) | 7,500                 | 596.25G                     | S30 (512G), $41.01/mo                                  | **$357.88**                                         | **$216.21**                                          |

{% hint style="info" %}
Case II, Standard IPC Device Management (Hardware, Network, Hard Disk, System), **187Tags/min**
{% endhint %}

| **Azure VM Tier (WinSrv 2019)**  | **Device** **Number** | **Storage** **Required/mo** | **Storage Tier (HDD) Recommended (Monthly Retention)** | **Price Estimation WinSrv 2016 + Storage (USD)/mo** | **Price Estimation Ubuntu 18.04 + Storage (USD)/mo** |
| -------------------------------- | --------------------- | --------------------------- | ------------------------------------------------------ | --------------------------------------------------- | ---------------------------------------------------- |
| D2sV5 (2 Cores 8G) ($158.46/mo)  | 10                    | 4.692G                      | S6 (64G), $3.06/mo                                     | **$161.52**                                         | **$90.66**                                           |
|                                  | 100                   | 44.22G                      | S10 (128G), $5.94/mo                                   | **$164.4**                                          | **$93.54**                                           |
|                                  | 500                   | 219.9G                      | S20 (512G), $21.81/mo                                  | **$180.27**                                         | **$109.41**                                          |
|                                  | 2,400                 | 1,061.28G                   | S40 (2,048G), $81.97/mo                                | **$240.43**                                         | **$169.57**                                          |
| D4sV5 (4 Cores 16G) ($316.87/mo) | 4,000                 | 1,759.2G                    | S40 (2,048G), $81.97/mo                                | **$398.84**                                         | **$257.17**                                          |

{% hint style="info" %}
Case III, Data Collection, **15Tags/sec**
{% endhint %}

| **Azure VM Tier (WinSrv 2019)**  | **Device** **Number** | **Storage** **Required/mo** | **Storage Tier (HDD) Recommended (Monthly Retention)** | **Price Estimation WinSrv 2016 + Storage (USD)/mo** | **Price Estimation Ubuntu 18.04 + Storage (USD)/mo** |
| -------------------------------- | --------------------- | --------------------------- | ------------------------------------------------------ | --------------------------------------------------- | ---------------------------------------------------- |
| D2sV4 (2 Cores 8G) ($158.46/mo)  | 10                    | 21.18G                      | S10 (128G), $5.94/mo                                   | **$164.4**                                          | **$93.54**                                           |
|                                  | 100                   | 209.1G                      | S20 (512G), $21.81/mo                                  | **$180.27**                                         | **$109.41**                                          |
|                                  | 300                   | 626.7G                      | S30 (1,024G), $41.01/mo                                | **$199.47**                                         | **$128.61**                                          |
|                                  | 800                   | 1,671.3G                    | S40 (2,048G), $81.97/mo                                | **$240.43**                                         | **$169.57**                                          |
| D4sV4 (4 Cores 16G) ($316.87/mo) | 1,300                 | 2,714.7G                    | S50 (4,096G), $163.84/mo                               | **$480.71**                                         | **$339.04**                                          |
