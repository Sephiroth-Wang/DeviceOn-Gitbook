# Cloud Versions

DeviceOn is based on a microservice design, each component is stateless and supports multiple instances for scale up. This results in heavily simplified deployment to WISE-PaaS (Cloud Foundry), Azure PaaS, standalone virtual machines or Kubernetes. Both public cloud and private cloud (on-premise) deployments are supported. This chapter provides an introduction and provides a summary of requirements for those scenarios. The container version of DeviceOn starts from version number **v-1.1.x** (WISE-PaaS/Azure Kubernetes), while the standalone version starts from **v-5.x.x.** The standalone version comprises of IoTHub, database (PostgreSQL and MongoDB), Dashboard (Grafana), Webservices (Tomcat) and DeviceOn core applications.

## Standalone Version (VM)

The standalone version provides all packages of the DeviceOn software in one installer package, including RabbitMQ as a message broker, MongoDB, PostgreSQL as databases, Grafana for visualization, Tomcat for web services, and a watchdog service that protects DeviceOn core components from crashing or becoming unresponsive.

This section specifies the minimum hardware requirements for DeviceOn Cloud (Standalone) and the operating systems on which DeviceOn is supported. In general, the better the hardware configuration of your computer, the better your experience with DeviceOn will be. To achieve a more satisfying experience with DeviceOn, particularly in terms of the client software, it is highly recommended that your system be substantially better than the minimum requirements specified in the following sections. This is particularly true if running server software locally on the same system as the client software.

Attention to the following areas can make a significant improvement to your overall user experience and enjoyment of the software:

* Memory - the more RAM your computer has, the better.
* CPU speed - the faster, the better.
* Hard Drive - the larger, the better.

General Operation Systems and Recommendations:

* <mark style="color:blue;">**Windows Server 2016 64-bits**</mark>
* <mark style="color:blue;">**Windows Server 2019 64-bits**</mark>
* <mark style="color:blue;">**Windows Server 2022 64-bits**</mark>
* <mark style="color:blue;">**Ubuntu 18.04/20.04 64-bits**</mark>

_Reserve Port for DeviceOn Server Used_

| Name & Description                           | Inbound Port                                                                      |
| -------------------------------------------- | --------------------------------------------------------------------------------- |
| DeviceOn HTTP, HTTPs Web Services            | 80, 443 \[Depends on Installation]                                                |
| DeviceOn Dashboard (Grafana)                 | 3000 \[Depends on Installation]                                                   |
| Message Broker (RabbitMQ) MQTT, MQTTs        | 1883, 8883                                                                        |
| Message Broker (RabbitMQ) AMQP, AMQPs        | 5671, 5672                                                                        |
| Message Broker (RabbitMQ) Management Console | 15672                                                                             |
| Repeater for Remote Desktop                  | <p>5501 (Releases before v4.6)<br>8022 (Releases after v4.7) Encrypted Tunnel</p> |
| Websockify for Remote Desktop                | 6083 (Releases after v4.6)                                                        |
| Database for MongoDB                         | 27017                                                                             |
| Database for PostgreSQL                      | 5432                                                                              |
| FTP Service                                  | 2121 \[Depends on Installation]                                                   |

Hardware Minimum Requirements:

* <mark style="color:blue;">**Intel® Core™ i5 2.3 GHz CPU and at least 8GB of RAM**</mark>
* <mark style="color:blue;">**25 GB root partition for the system**</mark>
* <mark style="color:blue;">**100 GB data storage partition (for documents and indexing)**</mark>

## DeviceOn for Azure (Enterprise Edition)

The Azure Kubernetes Service (AKS) makes it easy to deploy a managed Kubernetes cluster to Azure. AKS reduces the complexity and operational overhead of managing Kubernetes by offloading much of that responsibility to Azure. Azure handles critical tasks like health monitoring and maintenance for those Kubernetes services.

Deploying DeviceOn on the Azure Kubernetes Service is easy and with just a few steps, containers or nodes can be scaled up to manage thousands of devices. Moreover, DeviceOn can leverage the Azure IoTHub and Cosmos DB for Azure native security and performance. Since the data is already stored on the Azure cloud, it is much easier to leverage the Azure ecosystem – for example using the provided data for Azure Machine Learning. DeviceOn can be deployed to Azure Kubernetes directly from the WISE-Marketplace.

![](https://docs.wise-paas.advantech.com/dataSource/resource/1617092488995180160.png)

