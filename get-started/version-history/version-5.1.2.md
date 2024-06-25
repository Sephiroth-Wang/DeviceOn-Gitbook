# Version 5.1.2

## More Comprehensive and Intuitive Operation

### <mark style="color:blue;">Brand-New User Interface and Monitoring Experience for Devices</mark>

In order to enhance user comprehension of **real-time** sensor values and facilitate the configuration of the rule engine, we have introduced a consolidated monitoring interface. This interface combines both **device software and hardware monitoring**, presenting the information in an intuitive dashboard visualization. Each widget within the dashboard provides access to **historical data** as well as monitoring settings for the **rule engine**.

By integrating the device software and hardware monitoring, users can now conveniently track and analyze sensor data in one centralized location. The dashboard offers a comprehensive overview of the current sensor values, allowing users to assess their status at a glance. Furthermore, the inclusion of historical data within the widgets enables users to analyze trends, patterns, and anomalies over time, aiding in the fine-tuning of the rule engine.

To draw immediate attention to critical situations, the widgets are designed to display a warning red box when a sensor value surpasses a predefined threshold. This visual indicator quickly alerts users to potential issues, prompting them to take necessary actions promptly.

The new monitoring interface is aimed at improving usability and efficiency for users. By consolidating real-time sensor monitoring, historical data analysis, and rule engine configuration, it simplifies the process of understanding sensor values and optimizing system performance. Users can now leverage the power of the monitoring interface to gain valuable insights, make informed decisions, and ensure the smooth operation of their devices.

In summary, the newly introduced monitoring interface combines device software and hardware real-time monitoring in a dashboard visualization. It provides access to historical data and facilitates rule engine configuration within each widget. With this enhanced interface, users can better comprehend sensor values, analyze trends, and promptly address any deviations from the defined thresholds, ensuring optimal performance and reliability.

**System Monitoring**:

> CPU, memory, network, disk usage, and running processes are among the system monitoring components.

![](https://docs.wise-paas.advantech.com/dataSource/resource/1685348289638059397.png)

**Hardware Monitoring**:

> The hardware monitoring items include HDD health status, temperature, GPIO, fan speed, OSD/LVDS screen, voltage, current, and so on. The main sensors are provided by Advantech SUSI driver.

![](https://docs.wise-paas.advantech.com/dataSource/resource/1685348412206645943.png)

### <mark style="color:blue;">Application, Software Watchdog</mark> <a href="#font_colorblueapplication_software_watchdogfont_23" id="font_colorblueapplication_software_watchdogfont_23"></a>

DeviceOn incorporates a software watchdog, which serves as a vital mechanism to oversee the execution of software processes and guarantee their optimal performance. Acting as a timer or monitoring process, the software watchdog diligently verifies at regular intervals whether the software is operating as intended and remains functional. By continuously monitoring the software’s status, DeviceOn ensures the smooth and reliable operation of the processes, promptly identifying any potential issues and taking necessary actions to maintain system integrity. The software watchdog acts as a safeguard, providing reassurance that critical software processes are consistently running as expected, minimizing disruptions and optimizing overall performance.

![](https://docs.wise-paas.advantech.com/dataSource/resource/1685349549892641705.png)

In the event of errors, unresponsiveness, or exceeding CPU or memory thresholds, the system will proactively initiate appropriate actions such as process **Restart** or **Kill**. Users have the flexibility to define rules for specific processes by selecting them from the active process list. This empowers users to customize the system’s behavior and set guidelines for handling different scenarios. By allowing users to define rules based on their specific requirements, the system ensures efficient resource utilization, resolves potential issues, and maintains optimal performance.

![](https://docs.wise-paas.advantech.com/dataSource/resource/1685349427418399055.png)

## Enhancement

### <mark style="color:blue;">Upgrade Backup/Recovery to version 15</mark>

DeviceOn has recently upgraded Acronis to its latest version, 15, in order to provide compatibility with the latest hardware and operating systems. This update ensures that users can take advantage of Acronis’ enhanced features and functionalities while seamlessly operating on newer devices and platforms. The transition from version 12.5 to version 15 enables DeviceOn to deliver an improved user experience and better support for the ever-evolving technology landscape.

### <mark style="color:blue;">Stabilize and Improve the Quality of Remote Desktops</mark> <a href="#font_colorbluestabilize_and_improve_the_quality_of_remote_desktopsfont_37" id="font_colorbluestabilize_and_improve_the_quality_of_remote_desktopsfont_37"></a>

In our latest update, we are excited to enhancement a new feature that focuses on stabilizing and enhancing the quality of remote desktop experiences. We understand the critical importance of seamless remote access to workstations and servers, and we have designed this feature to address the common challenges faced by remote desktop users.

One of the primary objectives of this new functionality is to provide a stable and reliable connection for remote desktop users. We have implemented advanced algorithms and protocols that optimize network utilization, minimizing latency and packet loss. As a result, even when accessing resources while the movie is playing, the remote desktop experience is smoother and more responsive.

### <mark style="color:blue;">Batch Application Uninstall (App Store) and Device Data Upload are Supported</mark> <a href="#font_colorbluebatch_application_uninstall_app_store_and_device_data_upload_are_supportedfont_41" id="font_colorbluebatch_application_uninstall_app_store_and_device_data_upload_are_supportedfont_41"></a>

With Batch Application Uninstall, users can now remove multiple applications from their devices simultaneously, saving valuable time and effort. Instead of manually uninstalling applications one by one, this feature allows for a bulk uninstallation process. Administrators and users can select multiple applications from a list or define specific criteria to uninstall a group of applications in a single action. This greatly simplifies the application management process, particularly in environments with a large number of devices or where frequent software updates and changes occur.

In addition to Batch Application Uninstall, we have also introduced Device Data Upload functionality. This feature enables users to upload sensor data from their devices to our platform with ease.

## Third-Party Updates

* OpenJRE (v1.8.362)
* Tomcat (v9.0.73)
* RabbitMQ (v3.11.6), Erlang 25
* PostgreSQL (v14.2)
* MongoDB (v4.4.14)
* Grafana (v9.3.13)
