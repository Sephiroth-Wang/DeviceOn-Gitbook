# App Management (OTA)

App Store is an enhanced OTA software update feature which presented in a familiar mobile management user interface to provide users with the ability to manage their own exclusive applications and deploy them to remote devices in a simple way. App Store is divided into two modes of operation. IT administrators could use DeviceOn portal to customize, upload, manage apps and schedule installation to designated devices, which we call the manager mode. Second, in the client mode, the App Store application is built-in the device side, and the device can instantly update the applications.

{% embed url="https://www.youtube.com/watch?v=5wRANEF-nxM" %}

## App Store (Batch Deploy)

{% hint style="info" %}
_The perspective of **deploying to the device with the App**_
{% endhint %}

<figure><img src="https://i.imgur.com/H0lrQQ6.png" alt=""><figcaption></figcaption></figure>

1. **Keyword Search**: Input keyword to search apps.
2. **App List**: View all apps, grouping by category. Click to open a window to present App Information.

### Application Information

![](https://i.imgur.com/ve16wVH.png)

1. **Information**: Including all information about the app.
   * _Description_: Description text of app. Hidden in default, click \[More] to show all.
   * _Last Update_: Last update date of app.
   * _Operating System_: The app’s support operating system. It is relevant to version, might have different platforms between versions.
   * _Offered by_: The provider company of app. Click on it to show more information of the company, and all apps belongs to the company.
   * _Contact Support_: Contact person of the app.
   * _Keyword_: Keyword list of the app. Manager can search app by these keywords.
2. **Repository**: The file holder of the app. Select one of repositories to decide where app downloads from and getting app’s Version list
3. **Version**: The version number of the app.
4. **Install**: After select Repository and Version, click Install button to open the Install dialog, where manager can select Devices/Groups to run installation.

### Installation

![](https://i.imgur.com/lxryM30.png)

1. **Search Account or Group**: Input keyword to search account or group. It is useful when there are a lot of accounts below.
2. **Accounts and Device Groups**: List accounts, and Device Groups under each account. Check the Device Group will add all installable devices of the Device Group to Selected Device.
3. **Filter devices**: Turn On/Off the filter.
   * **If switch-on**: Device List shows devices which does not install the version of the app.
   * **If switch-off**: Device List shows devices which does not install the version of the app, and devices have installed app’s version is the same or beyond manager selected version. Default is “On” to prevent manager duplicating installing app with the same version.
4. **Selected Device**: Devices list here will install the app.
5. **Confirm**: Execute installation of the app to selected devices.
6. **Cancel**: Cancel this operation, back to previous step

## My Device (One-by-One Deploy)

{% hint style="info" %}
_From the perspective of **which apps can be installed on the device**_
{% endhint %}

<figure><img src="https://i.imgur.com/Gtk8EkW.png" alt=""><figcaption></figcaption></figure>

1. **Device Information**: Information of the device, click More to view full content
2. **Installed**: Show installed app of the device.
3. **Installed App**: Installed apps list.
4. **Suggested for the device**: Not installed apps list, or installed app has newer version.
5. **App Control Button**: Enabled button is colorful, otherwise button is fade-out.\
   \- **Upgrade**: The app can upgrade to newer version.\
   \- **Uninstall**: The app support uninstall ability; manager can uninstall the app online.

### Schedule App Upgrades for Device

![](https://i.imgur.com/Dz8I8u3.png)

1. **App Name**: Select an application and OS to upgrade.
2. **Upgrade Mode**: Decide how to upgrade when there are multiple versions beyond the app installed in the device currently. Maximum mode will upgrade to the latest version directly. Increment mode will upgrade from next version to the latest version by ascending sorted version.
3. **Execute Frequency**: Schedule executing frequency. By changing frequency option to set relevant setting. DeviceOn provide Daily, Weekly, Monthly, and Once to fit variable schedule needing.
4. **Save**: Click to save schedule setting.
5. **Cancel**: Discard changes and close this dialog.

### Schedule App Upgrades for Device Groups

<figure><img src="https://i.imgur.com/PXiclP5.png" alt=""><figcaption></figcaption></figure>

1. **Select Type**: Select Device Group to retrieve device group list or select Device to retrieve device list. Changing this option will affect result of list below.
2. **Device Group List**: Device groups are managed by Select Account will list here.
3. **More Option**: Click to more option.
   * _**Device Group Details**_: Open a dialog shows device group relevant information. e.g., group description, list of devices under the device group.
   * _**Device Group Schedule**_: Setting schedule to the device group. UI and setting are all the same with Device Schedule. And the schedule setting will apply to devices in the group, which are able to install/upgrade app.

## Repository

The Repository Management features allow configuring storage locations for app packages. Supported protocols include **Azure Blob**, **Amazon S3**, and **FTP**. Admins can create custom repositories or use the built-in Default-FTP server.

#### Key capabilities:

Upload app packages, Manage app versions, Edit app metadata like descriptions and icons. Package custom apps using the online wrapping tool.

#### Limitation:

* Maximum size of app package: 1.5 GB

{% hint style="info" %}
By default, a read-only device-upgrade repository is provided by Advantech for new DeviceOn Agent upgrades. Admins cannot modify or access packages in this repository directly.
{% endhint %}

<figure><img src="https://i.imgur.com/JmqnkMm.png" alt=""><figcaption></figcaption></figure>

1. **Repository List**: All repository’s list here. Select an option to show apps in the repository.
2. **Add/Edit Repository List**: Open a dialog to manage repository.
3. **Digital Signature**: DeviceOn provides a digital signature method for the software, leveraged with **Azure Key Vault** to verify the correctness of the **public key** and avoid _**Meet-in-the-middle attacks**_.
4. **Add an App**: Open online wrap tool to build an app.
5. **Upload an App**: Upload an app package files which are created by Online Wrap Tool.
6. **Remove an App**: Switch to remove mode, select app which manager want to remove, then click this button again to remove selected app.
7. **Deployment Log**: Provide app deployment records to view which device groups, devices the app is deployed to, success and failure history records, including execution time and detailed logs.
8. **App**: The app brief information. E.g. latest version number, update date, and support OS.
9. More Option: Click on **More** option shows **Add New Version**, **Version History** and **Edit App** Information.

For cloud storage, DeviceOn provide “**Amazon S3**”, “**Azure Blob**” and traditional **FTP** services. Next, we will describe how to configure and obtain the corresponding parameters.

### Amazon S3

You could create and get **Access Key**, **Secret Key** from Amazon Web service.\


<figure><img src="https://i.imgur.com/hXVp3XY.png" alt=""><figcaption></figcaption></figure>

* **Repository Name**: Your storage name, define by yourself.
* **Region**: Region of AWS S3
* **Access Key**: Access Key for AWS S3
* **Secret Key**: Secret Key for AWS S3

<figure><img src="https://i.imgur.com/EhS6EcI.png" alt=""><figcaption></figcaption></figure>

<figure><img src="https://i.imgur.com/OYR5d9s.png" alt=""><figcaption></figcaption></figure>

### Azure Blob

For Azure Blob, supports two mechanisms to access, one is “**Storage Account**” and “**Access Key**” with full access permission of container. The other is container **SAS token** generated via [Microsoft Azure Storage Explorer](https://azure.microsoft.com/zh-tw/features/storage-explorer/).\


<figure><img src="https://i.imgur.com/ONTz2q4.png" alt=""><figcaption></figcaption></figure>

*   Through Azure portal to get your **Storage Account** and **Access Key**.\


    <figure><img src="https://i.imgur.com/TR3KfGm.png" alt=""><figcaption></figcaption></figure>
* Get container’s **SAS token** via Azure Storage Explore, please make sure your permission (Read, Write, Delete, List) and valid period (Start and Expiry time)\
  ![](https://i.imgur.com/bMaQlYJ.png) ![](https://i.imgur.com/NXgokTM.png)

### FTP Service

You might set up your FTP server with security and account, password.\


<figure><img src="https://i.imgur.com/QZMf6VU.png" alt=""><figcaption></figcaption></figure>

* **Security**: Leave it as “NONE”, the default value. If your FTP server running on FTPS protocol, pick “FTPS”.
* **Storage Name**: Enter “MyFTP”.
* **Domain**: Enter the FQDN of your FTP server, or its IP address.
* **Port**: Should be 21 if the FTP server runs on a standard port number.
* **Account Name**: A valid username that can connect to the FTP server, and upload files onto the server as well.
* **Password**: The password to login.
* **CMC/SMC**: Maximum Client & Server Connection.
* **Root Path**: FTP server access path (root folder)
* **Description**: It’s optional information

### App Management

![](https://i.imgur.com/RaBzp3w.png)

1. **Operating System**: Select OS of the version can install.
2. **Version**: Version number. 3 or 4 digits and separated by dot(.). For example: 1.0.0 or 1.2.3.4
3. **Change Log**: Add your change log for the version, such as new features, bug fixed or any enhancement.
4. **Select Directory**: Select a directory to upload, which contains files are necessary for installing the app.
5. **Install Script**: Select a runnable script file for executing installation.
6. **Uninstall Option**: Switch On/Off to determine this version’s app can uninstall or not.
7. **Uninstall Script**: Select a runnable script file for executing uninstallation.
8. **Advanced Option**: Switch On/Off to show/hide more option.
9. **Reboot Option**: Switch On/Off to determine this version’s app need reboot after installation or not.
10. **Check Script**: Select a runnable script file for executing checking result of installation is successful or failed. The script file must return “**0**”, that means success, and all other value will be took as fail.
11. **Confirm**: After reviewing settings above, then click this button to start upload
12. **Cancel**: Discard changes and close this dialog.

### Create App

[How to Wrap and Upload your Application?](https://hackmd.io/2Stf3nPjQHydFRNg87Dsag#How-to-Wrap-and-Upload-your-Application)

{% embed url="https://www.youtube.com/watch?v=ltdo3xhLNzE" %}

\
