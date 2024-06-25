# Set up Device Thresholds and Enable Trigger Notifications

## Define a Threshold

In the "[**Real-time monitoring**](../web-user-interface/device-management/real-time-monitoring-and-rule-engine.md#real-time-monitoring)" page, you can click the icon ![](<../.gitbook/assets/image (106).png>) in the upper right corner of the sensor widget of interest to configure the **Rule Engine**.

<figure><img src="../.gitbook/assets/image (108).png" alt=""><figcaption></figcaption></figure>

#### IF Sections

* **Range**: You have the option to define the range, specifying values more than, less than, or both.
* **Lasting Time**: Indicates that the target device enters an abnormal condition only when it reaches the set threshold and remains in that condition for the set duration.
* **Notice Interval**: Specifies the frequency at which users receive an event notification until the condition returns to normal.
* **Custom Threshold Message**: Define a customized event log message of warning.

#### THEN Sections

* **Actions & Execution**: **When the set threshold is exceeded, you can choose the actions to be taken, such as** Power On/Off or **hardware control**, like GPIO control.
* **Trigger Frequency**: Set the trigger to "**Once**", "**Back to Normal**" or "**Always**."
* **Custom Action Messag**e: Define a customized event log message of action.

<figure><img src="../.gitbook/assets/image (107).png" alt=""><figcaption></figcaption></figure>

After configuring the Rule Engine, the Sensor Widget will have an additional <mark style="color:blue;">**yellow pointer**</mark>. Hovering over it will provide information about the set threshold value.

<figure><img src="../.gitbook/assets/image (109).png" alt=""><figcaption></figcaption></figure>

Additionally, within the **System Rule's Widget**, you can also check how many rule statuses are currently available.

<figure><img src="../.gitbook/assets/image (110).png" alt=""><figcaption></figcaption></figure>

* Rule Item: The number of rules that were created.
* Monitoring: The number of active rules.
* Out of Range: The number of rules that are out of range.

It provides a convenient way to manage and control the rules you have set up, making it efficient to make changes or **batch apply** ![](<../.gitbook/assets/image (24).png>) **the same rule to multiple devices simultaneously**.

<figure><img src="../.gitbook/assets/image (111).png" alt=""><figcaption></figcaption></figure>

## Enable Notification

Select a notification item for the **Threshold Category** and ensure your account's alert service is enabled

### Notification Item

<figure><img src="../.gitbook/assets/image (112).png" alt=""><figcaption></figcaption></figure>

### Personal Alert Services

Please go to your personal [**account settings**](../web-user-interface/account-management.md#notification) to enable or disable alert notifications for email, text messages, and social media."

<figure><img src="../.gitbook/assets/image (113).png" alt=""><figcaption></figcaption></figure>

{% hint style="danger" %}
_<mark style="color:blue;">**These alert services are personal setting**</mark>_. Please make sure the related services “[**Setting -> Notification**](../web-user-interface/system-setting.md#notification)” is configured, enabled on DeviceOn System.
{% endhint %}
