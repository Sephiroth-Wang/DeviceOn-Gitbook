# Update DeviceOn Server to the Latest Version

## Prerequisite <a href="#prerequisite" id="prerequisite"></a>

* A running DeviceOn server.
* To acquire the install program and make sure to have the latest version, please go to the [resource page](../#deviceon-server).

## Option 1 (Upgraded by the Installer) <a href="#option-1-upgraded-by-the-installer" id="option-1-upgraded-by-the-installer"></a>

Typically, the installation file of the new version can be used to upgrade the server. The service will be briefly suspended during the update process to allow for data backup and restore. As a result, the device will be offline for a brief period of time, and service will be unavailable.

#### Step-by-Step <a href="#step-by-step" id="step-by-step"></a>

*   **Step 1**: Launch the new installation and run as administrator\


    <figure><img src="https://i.imgur.com/IjeNqJZ.png" alt=""><figcaption></figcaption></figure>
*   **Step 2**: Click on ‘**Next**’\


    <figure><img src="https://i.imgur.com/my9QsQm.png" alt=""><figcaption></figcaption></figure>
*   **Step 3**: Select ‘**Upgrade**’ option to check your environment.\


    <figure><img src="https://i.imgur.com/8jb1XLl.png" alt=""><figcaption></figcaption></figure>
*   **Step 4**: Click on ‘**Install**’ to start to backup your server data and configuration and upgrade server version.\


    <figure><img src="https://i.imgur.com/KM8WoMH.png" alt=""><figcaption></figcaption></figure>

## Option 2 (Blue Green Deployment) <a href="#option-2-blue-green-deployment" id="option-2-blue-green-deployment"></a>

Blue/green deployment upgrades are strongly recommended if your server infrastructure operates on a public cloud with DNS and continuing production.

* **Step 1**: Download the latest version of [server installer](https://eiot.blob.core.windows.net/deviceon/DeviceOn\_Server.zip)
*   **Step 2**: Extract the zip file, there is a tool/folder called “**Server Migration**”.\


    <figure><img src="https://i.imgur.com/KPYMmCe.png" alt=""><figcaption></figcaption></figure>
*   **Step 3**: Copy the tool to your production server and start to backup data first.

    > Refer to [Server Migration>](../user-interface-and-functions/server-standalone/server-management-tools.md#server-migration)
* **Step 4**: Create a new VM and install the latest version of DeviceOn server.
* **Step 5**: Restore the data you backed up earlier and confirm that everything appears great.
* **Step 6**: To ensure that the device reconnects to a new VM, update the DNS record to the new VM and **stop the old VM**.
