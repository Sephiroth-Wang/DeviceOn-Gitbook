# Real-time Monitoring & Rule Engine

## Real-time Monitoring

In order to enhance user comprehension of **real-time** sensor values and facilitate the configuration of the **rule engine**, we have introduced a consolidated monitoring interface. This interface combines both device **software and hardware monitoring**, presenting the information in an intuitive dashboard visualization. Each widget within the dashboard provides access to **historical data** as well as monitoring settings for the rule engine.

By integrating the device software and hardware monitoring, users can now conveniently track and analyze sensor data in one centralized location. The dashboard offers a comprehensive overview of the current sensor values, allowing users to assess their status at a glance. Furthermore, the inclusion of historical data within the widgets enables users to analyze trends, patterns, and anomalies over time, aiding in the fine-tuning of the rule engine.

To draw immediate attention to critical situations, _the widgets are designed to display a warning **red box** when a sensor value surpasses a predefined threshold_. This visual indicator quickly alerts users to potential issues, prompting them to take necessary actions promptly.

The new monitoring interface is aimed at improving usability and efficiency for users. By consolidating real-time sensor monitoring, historical data analysis, and rule engine configuration, it simplifies the process of understanding sensor values and optimizing system performance. Users can now leverage the power of the monitoring interface to gain valuable insights, make informed decisions, and ensure the smooth operation of their devices.

In summary, the newly introduced monitoring interface combines device software and hardware real-time monitoring in a dashboard visualization. It provides access to historical data and facilitates rule engine configuration within each widget. With this enhanced interface, users can better comprehend sensor values, analyze trends, and promptly address any deviations from the defined thresholds, ensuring optimal performance and reliability.

<figure><img src="https://hackmd.io/_uploads/S19YU0FN6.png" alt=""><figcaption></figcaption></figure>

## Rule Engine

You can <mark style="color:blue;">**click on the icon**</mark> <img src="../../.gitbook/assets/image (21).png" alt="" data-size="original"> <mark style="color:blue;">**of each sensor widget**</mark> <mark style="color:blue;">**to set a rule for a specific condition**</mark>. For instance, let’s say you want to set a threshold for CPU usage, whether it should be **higher** or **lower** than a certain value. The “**lasting time**” refers to how long the sensor needs to stay above the threshold before triggering an action. This is to prevent sudden spikes in values from triggering unnecessary actions. The “**notice interval**” determines how often you want to receive notifications if the threshold continues to be exceeded. Finally, you have the option to define various **actions**, such as powering on or off your device, enabling or disabling monitors, setting GPIO pins to high or low, initiating a system lockdown, or simply doing nothing.

<figure><img src="../../.gitbook/assets/image (22).png" alt=""><figcaption></figcaption></figure>

Once you create a rule, you can easily see how many rules are being monitored and how many are out of range. Simply click on the number displayed on the widget or the information icon ![](<../../.gitbook/assets/image (23).png>). This will allow you to **disable**, **edit**, or **apply** the rule to multiple devices at once.\
![](https://hackmd.io/\_uploads/B13-3Mh8n.png)

It provides a convenient way to manage and control the rules you have set up, making it efficient to make changes or **batch apply** ![](<../../.gitbook/assets/image (24).png>) **the same rule to multiple devices simultaneously**.

{% hint style="info" %}
To apply the rule to other devices, please ensure that the applicable devices have the same hardware and software configuration, including the corresponding sensors, software process, and rule configuration, so that the rule could be applied ‘effectively’.
{% endhint %}

<figure><img src="../../.gitbook/assets/image (25).png" alt=""><figcaption></figcaption></figure>

You can refer to the Lab section for a more detailed standard operating procedure regarding the rule engine.

* [Set up the Device Thresholds and Enable Trigger Notifications](../../managed-devices/set-up-device-thresholds-and-enable-trigger-notifications.md)
* [Set up the Application Watchdog and Enable Trigger Notifications](../../managed-devices/set-up-the-application-watchdog-and-enable-trigger-notifications.md)

## Historical Data

You can click on the icon ![](<../../.gitbook/assets/image (26).png>) of each sensor widget to see the historical data, which will help you make decisions or understand the sensor’s past status. By default, the sensor reports data every 60 seconds. If you want more precise information, you can adjust the reporting interval by going to **Device -> Data -> Data Upload**. This way, you can get a better understanding of the sensor’s behavior and analyze its data in detail.\


<figure><img src="https://hackmd.io/_uploads/HkBQtGh82.png" alt=""><figcaption></figcaption></figure>

![](https://hackmd.io/\_uploads/B1kpFfhI2.png)

## **System Level**

### **CPU and Memory**

The system keeps track of how much the CPU and memory are being used in real-time. It does this by using a standard API provided by the device’s operating system. This allows you to monitor and see how much CPU and memory resources are being utilized by various processes on your device.

### **Network**

Some devices, like industrial PCs, can have multiple network cards. To switch between these different network cards, you can simply click on the angle brackets “**<**” and “**>**” on the device.

### **Device Manager (Hardware Sentinel)**

The Windows-only Device Manager console allows real-time monitoring of connected peripherals and hardware. It enables administrators to track USB-powered input devices, **external USB storage**, **monitors**, and **plug-and-play devices** on managed systems. DeviceOn leverages intelligent device recognition with continuous threat monitoring. The virtual sentinel can automatically trigger alerts per defined whitelist policies when detecting newly connected unauthorized or suddenly disconnected devices. This automated tracking and alert system enhances administrator visibility and control to identify threats from unapproved devices.

<figure><img src="https://hackmd.io/_uploads/HkvSvCK4p.png" alt=""><figcaption></figcaption></figure>

### **Hard Drive (Disk Usage)**&#x20;

In the **system tab**, we provide information about the hard drive that we are focusing on. This includes details about the **used space** and the **total available space** on the hard drive. By looking at the widget, users can quickly see the overall storage capacity of the disk, which includes all volumes and partitions.

<figure><img src="../../.gitbook/assets/image (28).png" alt=""><figcaption></figcaption></figure>

If you want more detailed information about the usage of specific partitions, you can find it in the “**Disk Partition**” widget. This will give you a breakdown of how each partition is being utilized and how much space is being used on each one.

### **Running Processes**&#x20;

<figure><img src="../../.gitbook/assets/image (27).png" alt=""><figcaption></figcaption></figure>

To perform certain actions on a specific process, such as **restarting** it, **terminating** (kill) it, or creating a **monitoring rule**, you can simply click on the “**More**” option. This will give you additional options and control over the process you’re interested in.

<figure><img src="https://hackmd.io/_uploads/H1xqW-oLn.png" alt=""><figcaption></figcaption></figure>

#### Application, Software Watchdog

If you want to create a monitoring rule for a specific process, you can click on “**Edit software watchdog rules**” for that process. This option allows you to customize and set up monitoring rules specifically tailored to that particular process.

<figure><img src="https://hackmd.io/_uploads/r1pqJQsI3.png" alt=""><figcaption></figcaption></figure>

For process monitoring, there are three conditions you can set. The first one is “**Not Exist/Not Responding**,” which means if the process doesn’t exist or stops responding. The second condition is when the **CPU usage** goes higher than a specified threshold, and the third condition is when the **memory used** exceeds a certain limit.

After setting the conditions, you can define the duration for which the condition needs to persist before triggering an action. This helps avoid unnecessary actions due to temporary fluctuations.

Next, you can choose a **trigger policy** that determines what action to take when the condition is met. You have options like always performing the action, sending a warning message, or setting a maximum number of times to trigger the action.

Lastly, you have various actions available to you. You can choose to kill the process, restart it, adjust the process priority, assign CPU affinity, or even launch a specific process as needed. These actions give you flexibility in managing and controlling processes based on your monitoring settings.

### Installed Program

That retrieves information from the Windows “**Add or Remove Programs**” feature. This could helps you view the list of programs installed on your device.\


<figure><img src="https://hackmd.io/_uploads/B1-24ZiIn.png" alt=""><figcaption></figcaption></figure>

## Hardware Level

When it comes to hardware monitoring, specifically for Advantech industrial PCs with SUSI driver support, we can also display additional information on the page. This includes the speed of the **CPU fan** (Revolution(s) Per Minute), **voltage** and **current** levels at the system and board level, **GPIO**, **temperature**, and display for **LVDS/OSD**.

<figure><img src="https://hackmd.io/_uploads/B12hQXhLh.png" alt=""><figcaption></figcaption></figure>

### **Hard Drive**

In the **hardware tab**, we provide information about the **hard drive healthy**, temperature and **S.M.A.R.T** that we are focusing on. The healthy is based on Acronis healthy model, that calculate on edge side, if you are interested, refer to the [official page](https://dl.acronis.com/u/software-defined/html/AcronisCyberInfrastructure\_4\_6\_admins\_cmd\_guide\_en-US/index.html?TocPath=Monitoring%2520the%2520storage%2520cluster%257CMonitoring%2520chunk%2520servers%257CMonitoring%2520disk%2520health%257C\_\_\_\_\_2#calculating-disk-health.html).\
![](https://hackmd.io/\_uploads/S1ztbQn8n.png)

![](https://hackmd.io/\_uploads/HJXXLQnLn.png)

For Advantech industrial SQ Flash, we provide advanced information, such as SSD performance, per day host & NAND Data Volume, Estimate life End, self-check and so on.\


<figure><img src="https://hackmd.io/_uploads/B1dcUQh83.png" alt=""><figcaption></figcaption></figure>

## **NVIDIA Jetson**

**NVIDIA® Jetson**™ is used by professional developers to create breakthrough AI products across all industries, and by students and enthusiasts for hands-on AI learning and making amazing projects. We provide a professional monitoring interface to show the status of your NVIDIA Jetson device. Such as, **CPU**, **RAM**, **GPU** status and **Frequency** and etc. To help AI developer realize the AI, GPU usage.\


<figure><img src="https://hackmd.io/_uploads/HyamlmhU2.png" alt=""><figcaption></figcaption></figure>
