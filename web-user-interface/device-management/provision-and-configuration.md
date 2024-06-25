# Provision & Configuration

For device provision, 3 types of need be _**batch**_ pre-configured. One is “**Power On**”, select which mode to enable device wake up. The others are 3rd party tool integration, **Acronis** to _backup/recovery_ your device system and **Trellix** for _white-list security protection_. To install 3rd tools, you must purchase the license and activate the product.

## Power On (Wake-On-LAN)

To power your device up, you might to configure the mode for your device. The mechanism is based on Wake-on-LAN to send magic packet to your device. The default mode is “**Direct Mode**”, if not previously configured before.

<figure><img src="https://i.imgur.com/DjShMKN.png" alt=""><figcaption></figcaption></figure>

### Direct Mode

There is a limitation on “**Direct Mode**”, the DeviceOn server and edge device must be on the same network.

### Agent Mode

{% hint style="info" %}
_Wake up the target computer via another computer within the same network_
{% endhint %}

Choose this method if there is a second computer (eg. a server) within the network of the target computer that is turned on permanently. In this case, you can use the second computer to wake up the target computer. The second computer acts as a kind of “middleman” to forward the wake-up request to the target computer.\


<figure><img src="https://i.imgur.com/88vfUCh.png" alt=""><figcaption></figcaption></figure>

### Repeater Mode

{% hint style="info" %}
_Wake up the target computer via its public address_
{% endhint %}

Choose this method if the target computer can be reached via a public address. This is the case if you have either a fixed, static IP through your Internet provider or if your router has a public domain address with the help of a dynamic DNS provider.

In these cases, you can configure DeviceOn in such a way that the target computer is woken through this address. The configuration effort of this method is higher and more complex than in **Agent Mode** because you have to set up your router accordingly.

## System Backup (Installation)

Select the free space size to create **Acronis Secure Zone** (Hidden Partition) to backup system partition.

{% hint style="danger" %}
The free space size must larger than system used
{% endhint %}

<figure><img src="https://i.imgur.com/q0w066x.png" alt=""><figcaption></figcaption></figure>

## System Protection (Installation)

<figure><img src="https://i.imgur.com/Kvw7zHI.png" alt=""><figcaption></figcaption></figure>

