# Set up the Application Watchdog and Enable Trigger Notifications

## Define a Threshold

In the "[**Real-time monitoring**](../web-user-interface/device-management/real-time-monitoring-and-rule-engine.md#real-time-monitoring)" page, you can click the icon ![](<../.gitbook/assets/image (106).png>) in the upper right corner of the process widget of interest to configure the **application watchdog**. Alternatively, click on the **number of running processes** to list the current user-level processes.

<figure><img src="../.gitbook/assets/image (115).png" alt=""><figcaption></figcaption></figure>

For the application you want to monitor, click on its **name** or **"More"** action to configure rules.

<figure><img src="../.gitbook/assets/image (116).png" alt=""><figcaption></figcaption></figure>

#### IF Section

* **Not Exist or Not Responding**: This indicates that alerts will be triggered if the process no longer exists or becomes unresponsive."
* **CPU**: CPU usage exceeds what percentage.
* **Memory**: Memory exceeds what KB/GB".
* **Duration**: When it reaches the set condition and remains in that state for the set duration.

#### Trigger Policy

* **Always**: Always trigger alerts, send the event log, and then perform the action.
* **Maximum Times**: Set the maximum number of times to send alerts and perform the action.

<figure><img src="../.gitbook/assets/image (117).png" alt=""><figcaption></figcaption></figure>

#### THEN Action Sections

* **Kill** - Terminate the application's processes.
* **Restart** - Relaunch the previously running application processes.
* **Priority** - Configure the process priority level (e.g. Realtime, High, Above Normal, Normal).
* **Affinity** - Designate which CPU cores the processes can run on.
* **Execute** - Initiate and start up processes for another application.

After configuring the application watchdog, you can also check how many rule statuses are currently available.

<figure><img src="../.gitbook/assets/image (118).png" alt=""><figcaption></figcaption></figure>

* Rule Item: The number of rules that were created.
* Monitoring: The number of active rules.
* Out of Range: The number of rules that are out of range.

It provides a convenient way to manage and control the rules you have set up, making it efficient to make changes or **batch apply** ![](<../.gitbook/assets/image (24).png>) **the same rule to multiple devices simultaneously**.

<figure><img src="../.gitbook/assets/image (119).png" alt=""><figcaption></figcaption></figure>



## Enable Notification

Select a notification item for the **Software Watchdog Category** and ensure your account's alert service is enabled

### Notification Item

<figure><img src="../.gitbook/assets/image (120).png" alt=""><figcaption></figcaption></figure>

### Personal Alert Services

Please go to your personal [**account settings**](../web-user-interface/account-management.md#notification) to enable or disable alert notifications for email, text messages, and social media."

<figure><img src="../.gitbook/assets/image (113).png" alt=""><figcaption></figcaption></figure>

{% hint style="danger" %}
_<mark style="color:blue;">**These alert services are personal setting**</mark>_. Please make sure the related services “[**Setting -> Notification**](../web-user-interface/system-setting.md#notification)” is configured, enabled on DeviceOn System.
{% endhint %}
