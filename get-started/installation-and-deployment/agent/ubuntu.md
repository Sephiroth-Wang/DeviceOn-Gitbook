# Ubuntu

## Prerequisite

If your platform is **Ubuntu 18.04/20.04 on Nvidia Jetson**, please execute the following commands to install the dependent libraries.

1. To download package information from all configured sources:

```bash
sudo apt update
```

2. To install the dependent libraries:

```bash
sudo apt install cmake curl libxml2 libx11-6 libxext6 libxtst6 libmosquitto1 sqlite3 xterm ethtool lua5.1 net-tools openssl libcurl4 gcc g++ make cmake libxml2-dev libx11-dev libxtst-dev libxext-dev libmosquitto-dev autoconf autotools-dev build-essential libtool zlib1g-dev libcurl4-openssl-dev libssl-dev -y
```

Once your DeviceOn server installed, you could start to follow steps to onboarding your edge device.

1. **Log in to the DeviceOn Cloud Service with Your Account and Password**

![](https://i.imgur.com/cs5FCGe.png)

2. **Download DeviceOn Agent and Setup on your Device**

> Please try to get and download the latest version of [DeviceOn Agent installer](https://eiot.blob.core.windows.net/deviceon/WISE-Agent%20for%20v5.0.zip) for Linux version from [resources page](../../../#deviceon-agent).

3. **Open a terminal**

> The installer runs in CLI (Command Line Interface) mode. As such, open a terminal preferable for you.

4. **Copy the installer to target host**

> Use the way you like to copy the installer to the target host.

5. **Set the installer as executable**

> In the terminal, run “**chmod 0755 deviceonagent-Ubuntu\_20.04-x86\_64-2.x.x.0.run**” so that the installer as an executable file under Ubuntu Linux.

![](https://i.imgur.com/QFAf258.png)

## DeviceOn Agent Installation

6. **Running the installer**

> Change your working directory to where the installer is and run “**./deviceonagent-Ubuntu\_20.04-x86\_64-2.x.x.0.run**”. You may need to run “**sudo ./deviceonagent-Ubuntu\_20.04-x86\_64-2.x.x.0.run**” to acquire higher privileges if you were logged in as a normal user.

<figure><img src="../../../.gitbook/assets/image (178).png" alt=""><figcaption></figcaption></figure>

7. **Start DeviceOn Agent and Connect to DeviceOn**

> Change your directory to /usr/local/AgentService and run **sudo ./setup.sh** to answer connection information, such as credential URL, IoT Key, Device Name and etc.

<figure><img src="../../../.gitbook/assets/image (176).png" alt=""><figcaption></figcaption></figure>

* **Listen port for Web Service**: Please specify your preferred port number to access the DeviceOn Agent Portal. The port number must be within the allowable range and not conflict with any other services on your network.&#x20;
* **Listen port for WebSocket**: Specify a designated port for internal WebSocket communication.
* **Enter Credential URL and IoT Key** that information could retrieve from the DeviceOn portal.

![](https://hackmd.io/\_uploads/HkGVWudNa.png)

* **Assign device to User Account**: You can bind the target device into a “Default” group in your account on the portal automatically.
* **Enable TLS**: Turn ON/OFF the TLS/SSL mode.
* **Input Device Name**: Give your device name and show it on the portal.
* **Input AMT ID and password**: If your device support Intel AMT, please enter AMT ID and Password to enable these functions.
* **Input DASH ID and password**: If your device support AMD DASH, please enter DASH ID and Password to enable these functions.
* **Select KVM Mode** \[0: default, 1: Custom VNC, 2: disable]: User can use our default VNC to support the Remote Desktop function by entering 0 and give a listen port if you don’t want to use the default port. Second, select Custom Mode, if they already have a VNC server by entering 1 and provide the listen port and password. To disable the KVM function by entering 2.

8. **Open DeviceOn Agent Portal**

> Upon completing the installation steps, it is required to sign in to the DeviceOn Agent Portal and update the default password to activate the DeviceOn Agent.
>
> (The URL of DeviceOn Agent Portal listed during installation process.)

<figure><img src="../../../.gitbook/assets/image (179).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (180).png" alt=""><figcaption></figcaption></figure>

> When you run into this step the question shows like above, device is connected and under your account. To confirm the connection status via **agent\_status**:\
> 0: Disconnect, 1: Connected, 2: Connecting.

```bash
cat /usr/local/AgentService/agent_status
```



## **Start Device Management**

> By default, two “**Real-time Actions**” are created for a group, one is “**Screenshot**” and the other one is “**Reboot**”. The overview page further shows the online status of registered.

![](https://i.imgur.com/30uFMjk.png)
