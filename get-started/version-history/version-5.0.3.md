# Version 5.0.3

## More Comprehensive and Intuitive Operation

### <mark style="color:blue;">Open AMT Cloud Toolkit</mark>

The **Open Active Management Technology Cloud Toolkit (Open AMT Cloud Toolkit)** provides open-source, modular microservices and libraries for integrating Intel® Active Management Technology (Intel® AMT). The **Out-of-Band Management (OOB Management)** toolkit for Intel vPro® Platforms is an open source implementation that makes it simpler for IT departments and independent software suppliers (ISVs) to adopt, integrate, and customize OOB Management solutions.

The earlier version of DeviceOn was tightly linked with AMT, but the key drawback was that it could not span multiple networks, particularly when the server was placed in the public cloud. This limitation is solved by using Open AMT. Once the AMT device has been set up, it will actively connect to the Open AMT server, and DeviceOn offers an interface to bond with Open AMT to achieve full out-of-band administration of the device.

![](https://docs.wise-paas.advantech.com/dataSource/resource/1671418171564042525.png)

> [How to Manage iAMT Device through Open AMT and Integrate into DeviceOn](../../out-of-band/intel-amt/cross-network-integration-open-amt.md)

{% embed url="https://www.youtube.com/watch?list=TLGGhq0Tm9QQFR8yODExMjAyMw&v=L-aVQBuHa3A" %}

### <mark style="color:blue;">File Synchronization</mark> <a href="#font_colorbluefile_synchronizationfont_12" id="font_colorbluefile_synchronizationfont_12"></a>

**File synchronization** mostly assists in synchronizing files on the device to cloud storage. Users simply need to place the data in the default folder (**/WISE-Agent/FileSync**) in order for it to be synced. In some AI application scenarios, the device will continuously gather photos or video and submit them to the AI training platform for further training. Formerly, these raw data had to be manually operated on each device. DeviceOn allows you to collect video, audio, or image data on the device side in groups, which can save you a lot of time. Furthermore, if you are concerned about security, DeviceOn allows you to encrypt files on the device before uploading them to avoid sensitive data leaks.

![](https://docs.wise-paas.advantech.com/dataSource/resource/1671429987402587072.png)

### <mark style="color:blue;">Device System Log</mark> <a href="#font_colorbluedevice_system_logfont_17" id="font_colorbluedevice_system_logfont_17"></a>

Remotely gather and download device logs instantaneously, and support Windows/Linux to make diagnosing potential system faults easier.

![](https://docs.wise-paas.advantech.com/dataSource/resource/1671430401135495968.png)

![](https://docs.wise-paas.advantech.com/dataSource/resource/1671430423521161038.png)

## Security Topic

### <mark style="color:blue;">Upgrade Apache Commons Text v1.10.0</mark>

Upgrade to the latest release of Apache Apache Commons Text to v1.10.0 and address false positive concerns with some vulnerability scanners.

### <mark style="color:blue;">Open SSL v3.0.7</mark> <a href="#font_colorblueopen_ssl_v307font_29" id="font_colorblueopen_ssl_v307font_29"></a>

Upgrade to the latest release of Open SSL to v3.0.7

### <mark style="color:blue;">Secure Traffic Management and Control</mark> <a href="#font_colorbluesecure_traffic_management_and_controlfont_32" id="font_colorbluesecure_traffic_management_and_controlfont_32"></a>

For all control commands, improve the security of transmission from the device (**v-1.4.49**) to the server (**v-5.0**). Versions after version 5.0 are compatible with previous and new versions of WISE-Agent. **Please note that you must use the** [**v-1.4.45**](https://eiot.blob.core.windows.net/deviceon/WISE-Agent.zip) **versions of WISE-Agent for the 4.x (server) version.**

## Third-Party Updates

* OpenJRE (v1.8.0\_292-1)
* Tomcat (v9.0.63)
* RabbitMQ (v3.11.6), Erlang 25
* PostgreSQL (v14.2)
* MongoDB (v4.4.14)
* Grafana (v7.3.10)
