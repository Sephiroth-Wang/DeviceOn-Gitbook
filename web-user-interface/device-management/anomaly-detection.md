# Anomaly Detection

DeviceOn Anomaly Detection Service (ADS) is one of the services that combines anomaly detection algorithm and DeviceOn function. It not only gives customers the high accuracy identification of the error message when advertising is getting interruption but also provides the IoT device remote monitoring and management. Leverage with _**Azure Custom Vision**_ to continually train the algorithm in order to overcome various errors pop-up under real field.

{% hint style="warning" %}
Before to detect your anomaly screen, please make sure your device is logged in to capture screen status.
{% endhint %}

Click the  icon to enter your API server **URL** and **API Key**.

<figure><img src="https://i.imgur.com/6aotHLj.png" alt=""><figcaption></figcaption></figure>

* **API URL & Key**: Please contact us for AI machine URL and Key, otherwise, deploy total package from Azure Marketplace.
* **Maximum Retention Days**: Maximum retention days for the warning images.
* **Interval**: _**Minimal interval**_ to detect devices screen.
* **Pop-up Window**: Enable to detect popup window on the devices.
* **Screen Frozen**: Enable to detect freezing window on the devices.

Second, create a rule for your device and define the **interval** that to capture the image for inference.

<figure><img src="https://i.imgur.com/KTxdsao.png" alt=""><figcaption></figcaption></figure>

If a screen freeze or any pop-up window is detected, it will be displayed here and dynamically marked with errors

<figure><img src="https://i.imgur.com/9cS8TxE.png" alt=""><figcaption></figcaption></figure>

You can also view the screen changes of these abnormal devices through historical records.

<figure><img src="https://i.imgur.com/e7oUkF1.png" alt=""><figcaption></figcaption></figure>
