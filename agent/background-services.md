# Background Services

## **Main Service**

The main service for connecting to the DeviceOn server/cloud is called “**DeviceOnAgent**” on Windows or “**saagent.service**” on Linux. This service is configured to start **manually** by default.

The other related service is “**DeviceOnAgent Portal**” on Windows or “**deviceonagentwebservice.service**” on Linux. This provides the web interface and is configured to start automatically. It will launch the **DeviceOnAgent** service on startup.



{% tabs %}
{% tab title="Windows" %}
<figure><img src="../.gitbook/assets/image (69).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Linux" %}
To confim the connection status on Linux through **agnet\_status**:\
0: Disconnect, 1: Connected, 2: Connecting.

```bash
cat /usr/local/AgentService/agent_status
```

* To update remote server IP:

```bash
sudo sed -i "s/CURRENT_IP/NEW_IP/g" /usr/local/AgentService/agent_config.xml
sudo systemctl restart saagent.service
```

<figure><img src="https://i.imgur.com/FEpKeT8.png" alt=""><figcaption></figcaption></figure>

* To update IoT Key or Credential URL:

```bash
sudo vi /usr/local/AgentService/agent_config.xml
```

Update CrdentialURL and IoTKey tag value and save, then restart the saagent.service.
{% endtab %}
{% endtabs %}

## **Watchdog Service**

The “**SAWatchdog**” service is a basic watchdog governing “**DeviceOnAgent** (Windows), **saagent.service** (Linux)” in order to ensure service quality.

{% tabs %}
{% tab title="Windows" %}
<figure><img src="../.gitbook/assets/image (70).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Linux" %}
To list only the running services on linux, we run:

```bash
systemctl --type service --state running
```

![](https://i.imgur.com/RCkvG9f.png)
{% endtab %}
{% endtabs %}
