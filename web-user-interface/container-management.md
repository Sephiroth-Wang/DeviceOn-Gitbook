# Container Management

Device container management is the major feature in this release, you can easily set up, deploy, monitor, and manage each container on different devices. For device managers, it can create, manage and set the health of containers within minutes, and provide a variety of container restart strategies. Through the dashboard, you can quickly understand the running status of the container in the managed device. In addition, for container developers, the [Azure Container Repository](https://azure.microsoft.com/en-us/services/container-registry/) is supported as a public cloud solution, and private cloud uses [Harbor](https://goharbor.io/) as a container repository.

{% embed url="https://www.youtube.com/watch?v=KAZJlm3aVQw" %}

## Dashboard

Through the dashboard, DeviceOn provides the summary of device docker status, for example how many container, images, volumes, and networks on that edge device.

<figure><img src="../.gitbook/assets/image (76).png" alt=""><figcaption></figcaption></figure>

## Container

* **Management and Actions**

Click on the Containers to shows details, you can choose the existing container to start, stop, restart, pause and other operations.

<figure><img src="https://i.imgur.com/FyxAJ7t.png" alt=""><figcaption></figcaption></figure>

After the container is started, you can click the Log, Status icon to know the running status of the current container in time, including Memory, CPU, and Network usage.

<figure><img src="../.gitbook/assets/image (77).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (78).png" alt=""><figcaption></figcaption></figure>

* **Deploy a Container to Edge Device (One and Batch)**

Click on “**+**” icon to create/deploy a container from remote registry.\


<figure><img src="https://i.imgur.com/fcmGcE6.png" alt=""><figcaption></figcaption></figure>

![](https://i.imgur.com/rcfYTBQ.png)

* **Mode**: If you want to deploy images in batches, you can click the **Group Mode**, otherwise you can select the **Device Mode**.
* **Container Name**: Given your container name.
* **Auto Start**: After the image is deployed, do you need to start running as a container immediately?
* **Remaining Storage**: Free space on hard drive
* **Source Image**: The source image can be the repository that has been set or the device itself.
* **Container Settings**: Parameter settings for container startup, such as port mapping, command, etc.

## **Images, Volumes, Networks Information**

* **Images**

Details of the image, including layer of content, environment variable Tag, ID, etc.\


<figure><img src="https://i.imgur.com/2uYbSEG.png" alt=""><figcaption></figcaption></figure>

* **Volumes**

Volume basic information and mount path of the device.

<figure><img src="https://i.imgur.com/yG4UEYs.png" alt=""><figcaption></figcaption></figure>

* **Networks**

Network information and which container used.

<figure><img src="https://i.imgur.com/bOLri3E.png" alt=""><figcaption></figcaption></figure>

## Registry

* **Configure Container Registry**

To add a container registry, go to **Container** > **Registries** and click the **+** icon. DeviceOn supports **Azure Container Registry (ACR)** for public registries and Harbor for private registries.

To configure an ACR registry:

1. Get the Registry URL, Username, and Token (Password) from ACR
2. Enter those details when creating the registry in DeviceOn

<figure><img src="https://i.imgur.com/CoQ8trG.png" alt=""><figcaption></figcaption></figure>

![](https://i.imgur.com/8NGrIOd.png)

* **Synchronize Registry**

\
Select your registries and click on ![](<../.gitbook/assets/image (79).png>) icon to synchronize the docker image list to DeviceOn\
Next, the repository and image listing information is displayed on DeviceOn, and you can start deploying these images to edge devices.

<figure><img src="https://i.imgur.com/kqSVM8m.png" alt=""><figcaption></figcaption></figure>

<figure><img src="https://i.imgur.com/h1Mu8w3.png" alt=""><figcaption></figcaption></figure>

