# Upgrade DeviceOn Agent in On-premises DeviceOn Server

Here is an example description of how to upgrade DeviceOn Agent in On-premises DeviceOn Server, for devices which do not have internet connectivity.

In closed network environment. On-premise DeviceOn Server can't download the latest released DeviceOn Agent through internet. Maintainer can upload DeviceOn Agent package manually then upgrade managed devices.

## Prerequisite

* A running DeviceOn Server.
* A device with installed DeviceOn Agent, that connects to the DeviceOn server.
* DeviceOn Agent package files.

## Upload DeviceOn Agent package

<figure><img src="../../.gitbook/assets/image_1719810711144.png" alt=""><figcaption><p>On-premises DeviceOn Serve, the App Store will be empty.</p></figcaption></figure>

Prepare DeviceOn Agent package files:&#x20;

* `DeviceOnAgent({PLATFORM})-{VERSION}-{HASH}.zip`&#x20;
* `DeviceOnAgent-data-{VERSION}-{HASH}.zip`

<figure><img src="../../.gitbook/assets/2024-07-01_124227.png" alt=""><figcaption><p>Using DeviceOn Agent 2.0.16 as example</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/2024-07-01_122943.png" alt=""><figcaption><p>Upload DeviceOn Agent package files to Repository</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/2024-07-01_124305.png" alt=""><figcaption><p>Choose DeviceOn Agent package files</p></figcaption></figure>

After upload process finished, DeviceOn Agent list in Repository

<figure><img src="../../.gitbook/assets/2024-07-01_124356.png" alt=""><figcaption></figcaption></figure>

## Upgrade DeviceOn Agent

<figure><img src="../../.gitbook/assets/2024-07-01_124440.png" alt=""><figcaption><p>Upgrade selected device</p></figcaption></figure>
