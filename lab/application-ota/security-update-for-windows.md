# Security Update for Windows

Here is an example description of how to perform Windows Security Updates on endpoint devices using DeviceOn, for devices that do not have internet connectivity:

DeviceOn can be used to deploy Windows security updates to endpoint devices that are not connected to the internet. The user can first download the latest Windows security update files from the [**Microsoft website**](https://support.microsoft.com/en-us/topic/windows-10-and-windows-server-2019-update-history-725fc2e1-4443-6831-a5ca-51ff5cbcb059), such as KB1234567.msu. Upload these update files to the DeviceOn's App store.

Then in the DeviceOn console, create an Application and select the Windows update file as the content for that Application. In the Deployment page, configure the deployment targets, such as selecting the device groups or devices to update.

DeviceOn will then push the Windows security update as an Application to the configured endpoints. When the device receives the update, it will automatically install the Application to perform the Windows security update.

In this way, the Administrator can use DeviceOn to regularly deploy security updates to Windows endpoints that are not internet-connected, in order to ensure the systems remain secure.

## Prerequisite <a href="#prerequisite" id="prerequisite"></a>

* A running DeviceOn server.
* A device which running on Windows operating system and installed DeviceOn Agent, that connects to DeviceOn server.
* A cumulative update for your **Windows version and Build number.** It can be downloaded from [Microsoft website](https://support.microsoft.com/en-us/topic/windows-10-and-windows-server-2019-update-history-725fc2e1-4443-6831-a5ca-51ff5cbcb059).  For example <mark style="color:purple;">**Windows 10 version**</mark>**&#x20;1809**. Please make sure the Windows version and build number on your device matches the requirements for this cumulative update. Installing the wrong cumulative update can cause issues, so it's important to verify your current OS build before installing.

<figure><img src="../../.gitbook/assets/image (121).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (124).png" alt=""><figcaption></figcaption></figure>

## Download Cumulative Update

Review Microsoft's documentation for details and system requirements before updating. Verify your OS build meets the prerequisites. Follow any prep steps noted. Then download the latest cumulative update for your Windows version from the Microsoft Update Catalog. Confirm it matches your build.

<figure><img src="../../.gitbook/assets/image (125).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (126).png" alt=""><figcaption></figcaption></figure>

## Confirm the Update

I recommend validating the Windows security update on a test device first before packaging it for OTA deployment. Windows security updates (MSUs) support a silent installation mode with the **/quiet** parameter. You can add **/quiet** to the command in your script to enable unattended installation. For example,&#x20;

```batch
windows10.0-kb5033911-x64-ndp48_fd9c7de7eff3906ed882d2a338030d33ea373ba5.msu /quiet
```

Testing the silent update on a sample device before wide rollout helps catch any potential issues and ensures the silent mode works properly. Once you've confirmed the silent update installs correctly, you can then package the script into an OTA update that can be deployed at scale.

{% hint style="info" %}
If your systems need multiple KB security updates, I recommend creating separate OTA packages to deploy each patch individually. Only include one security update per OTA package. After installing each patch, reboot the device before deploying the next one. Updating one KB at a time and rebooting in between helps avoid potential issues from applying multiple patches together.
{% endhint %}

After deploying the security update, you can validate it installed properly by checking for the corresponding KB in the system. To do this, go to Settings > Update & Security > Windows Update and click on Update history. This will show all of the installed updates on the device. Look for the specific KB number of the security update you deployed and verify it is listed as installed.

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>
