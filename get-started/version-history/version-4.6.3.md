# Version 4.6.3

## More Comprehensive and Intuitive Operation

### Container Management System

Device container management is the major feature in this release, you can easily set up, deploy, monitor, and manage each container on different devices. For device managers, it can create, manage and set the health of containers within minutes, and provide a variety of container restart strategies. Through the dashboard, you can quickly understand the running status of the container in the managed device. In addition, for container developers, the [Azure Container Repository](https://azure.microsoft.com/en-us/services/container-registry/) is supported as a public cloud solution, and private cloud uses [Harbor](https://goharbor.io/) as a container repository.

<figure><img src="https://docs.wise-paas.advantech.com/dataSource/resource/1654495142011123860.png" alt=""><figcaption></figcaption></figure>

<figure><img src="https://docs.wise-paas.advantech.com/dataSource/resource/1654495131423860195.png" alt=""><figcaption></figcaption></figure>

* **Management AI Inference Container on Advantech AIR-020 (NVIDIA Jetson) through DeviceOn**

{% embed url="https://www.youtube.com/watch?list=TLGGCVDBWBxHIKEyODExMjAyMw&v=bilP6FpyU0M" %}

* **Container Management (Monitoring, Deploy, and Logs) through DeviceOn Platform**

{% embed url="https://www.youtube.com/watch?list=TLGGzygpiCpZQYYyODExMjAyMw&v=KAZJlm3aVQw" %}

## Enhancement

### Server Configuration Tool

During DeviceOn Server installation, you will be asked to enter a fixed IP or domain name to allow the edge device to connect. In some cases, your server may need to re-adjust the IP of the server due to the configuration of the IT network environment, the update of SSL, etc. , you could make quick adjustments through this tool without manually modifying or reinstalling the DeviceOn server.

Second, it provides a mechanism that allows you to modify the suffix of the root account and adjust the automatic data recycling of MongoDB data (capped collection). Please note that when your database is larger, it will take longer to enable this function.

<div align="center">

<img src="https://docs.wise-paas.advantech.com/dataSource/resource/1654485454619315371.png" alt="">

</div>

### Server Migration <a href="#font_colorblueserver_migrationfont_27" id="font_colorblueserver_migrationfont_27"></a>

With the built-in “DeviceOn Server Migration” in this version, you can seamlessly transfer the physical device or VM with DeviceOn Server installed to the new hardware or a public cloud VM (AWS/Azure). The migration content includes your original device information, account information, configuration, etc. Note that this tool is only available after DeviceOn v-4.4.2

<div align="center">

<img src="https://docs.wise-paas.advantech.com/dataSource/resource/1654485436179386129.png" alt="">

</div>

## Third-Party Updates

* OpenJRE (v1.8.0\_292-1)
* Tomcat (v9.0.63)
* RabbitMQ (v3.8.19), Erlang 24
* PostgreSQL (v14.2)
* MongoDB (v4.4.14)
* Grafana (v7.3.10)
