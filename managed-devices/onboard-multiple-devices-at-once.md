# Onboard Multiple Devices at Once

{% hint style="info" %}
DeviceOn Agent will connect to DeviceOn server through **Credential URL** and **IoT Key** and those setting in **agent\_config.xml**, if you have many devices (that has DeviceOn Agent in it) need to connect to the server, it takes time to modify agent\_config.xml in each device. Here, we build-in the “**Local Provision**” Plugin to speed up this process. You will learn how to trigger all local devices to connect to the server with the same Credential URL and IoT Key.



The DeviceOn Agent local provision plugin will send Credential URL and IoT key to other local agent devices, and the local agent devices can connect to the server successfully. In following figure, you can send trigger command to make device A and B connect to a server with a Windows GUI tool.
{% endhint %}

<figure><img src="../.gitbook/assets/image (19).png" alt=""><figcaption></figcaption></figure>

## Prerequisite <a href="#prerequisite" id="prerequisite"></a>

* All devices must install DeviceOn Agent in it.
* All devices and the control PC must in the same local network (The multicast packet will not be filtered)
* All devices have the capability to connect to DeviceOn server.

## Steps to Local Provisioning <a href="#steps-to-local-provisioning" id="steps-to-local-provisioning"></a>

* **Step 1**: Download and unzip the [local provision GUI tool](https://eiot.file.core.windows.net/deviceon-dev/LocalProvision-win32-x64.zip?st=2020-04-01T01%3A25%3A36Z\&se=2030-04-02T01%3A25%3A00Z\&sp=rl\&sv=2018-03-28\&sr=f\&sig=J5gFP17SMdVXrSf%2BUfF7WN8WV8XVa3zCW0C0EnzweaY%3D).
*   **Step 2**: Place valid “**agnet\_config.xml**” file (with correct Credential URL and IoT Key) to “GUI tool\resources\tools” folder\


    <figure><img src="https://i.imgur.com/IKCmbD7.png" alt=""><figcaption></figcaption></figure>
*   **Step 3**: Double click “**LocalProvision.exe**”\


    <figure><img src="https://i.imgur.com/2nSYEid.png" alt=""><figcaption></figcaption></figure>
*   **Step 4**: Click Discover button\
    If windows display a firewall dialog, please click allow to enable TCP server permission in tool.

    <figure><img src="https://i.imgur.com/KZ0IDXe.png" alt=""><figcaption></figcaption></figure>

    <figure><img src="https://i.imgur.com/N3twPix.png" alt=""><figcaption></figcaption></figure>
*   **Step 5**: Wait for 10 second and then you can get the devices on checkbox list\


    ![](https://i.imgur.com/jaZ2n5r.png)

    <figure><img src="https://i.imgur.com/rCfOtEl.png" alt=""><figcaption></figcaption></figure>
*   **Step 6**: Pick-up the device that you would like to connect to the server and click **Active**.\


    Until now, the checked devices should connect to server after few second later.

    <figure><img src="https://i.imgur.com/KCVY47R.png" alt=""><figcaption></figcaption></figure>
