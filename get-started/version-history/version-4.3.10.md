# Version 4.3.10

## More Comprehensive and Intuitive Operation

### <mark style="color:blue;">Industrial IoT monitoring with InfluxDB (Time-Series Database)</mark>

The solution to provide real-time insight and analytics for your manufacturing process — collecting, storing and visualizing sensor data from your sensors, devices and industrial equipment. Over the past few years, the IoT community has embraced InfluxDB as a cornerstone of the solutions they build. Whether modernizing or greenfield, InfluxDB has helped many in working with vast quantities of sensor and device data.

<div align="center">

<img src="https://docs.wise-paas.advantech.com/dataSource/resource/1620962566372780802.png" alt="">

</div>

### <mark style="color:blue;">Now, DeviceOn officially fully supports InflubDB v2 for IoT Data</mark> <a href="#font_colorbluenow_deviceon_officially_fully_supports_influbdb_v2_for_iot_datafont_10" id="font_colorbluenow_deviceon_officially_fully_supports_influbdb_v2_for_iot_datafont_10"></a>

DeviceOn will automatically collect your IoT data and store in InfluxDB. Through the features of influxDB, data insight and analytics can be accelerated.

* **Scalability**\
  Collecting event data from your equipment is just the beginning. True digital transformation requires more data sources and more analysis of the combined data to gain a better understanding of your systems. InfluxDB is a high-performance data store written specifically for time series data. It allows for high throughput ingest, compression and real-time querying.
* **Open**\
  With the availability of so many open source tools, operators are no longer required to purchase arcane closed source solutions. Instead, they can look to building their own data historian replacements or buy a ready-made solution that is based on open source. This provides the operator with the freedom to quickly innovate and never be locked in to a single solution that could easily and quickly become obsolete.
* **Built for developers**\
  InfluxDB provides write and query capabilities with a command-line interface, a built-in HTTP API, a set of client libraries (e.g., Go, Python, and JavaScript) and Telegraf plugins for common data formats such as OPC-UA, ModBus, MQTT and more. In addition, the Influx Community is diverse and highly motivated, making contributions in code, documentation, and advocacy for the InfluxDB and Telegraf projects.

### <mark style="color:blue;">Event Log Analytics and Mutiple User Management</mark> <a href="#event_log_analytics_and_mutiple_user_management_23" id="event_log_analytics_and_mutiple_user_management_23"></a>

In order to make it easier and faster for the IT or operator to understand the current or historical equipment status, we have improved the Event Log analysis. You can find the problematic equipment or any abnormal events in the system from the dashboard at a glance.

<div align="center">

<img src="https://docs.wise-paas.advantech.com/dataSource/resource/1620960865882008310.png" alt="">

</div>

### <mark style="color:blue;">Increase Data Write Performance over 30%</mark> <a href="#increase_data_write_performance_over_30_27" id="increase_data_write_performance_over_30_27"></a>

DeviceOn re-optimizes and adjusts the storage mechanism for the data model of the IoT devices and supports the two most popular databases (**MongoDB**, **InfluxDB**) at the same time, and improves the performance by about **30%** compared with the previous version (v-4.3.3).

### <mark style="color:blue;">Continuous Notification and IoT Data Feeder</mark> <a href="#continuous_notification_and_iot_data_feeder_30" id="continuous_notification_and_iot_data_feeder_30"></a>

In response to third-party IoT integration applications, proactively push data to third parties. Developers no longer need to obtain data through the Restful API (polling). This **WebSocket** mechanism is not only more instantaneous but also saves network resources.

### <mark style="color:blue;">Industrial Display Monitor and Adjusting</mark> <a href="#industrial_display_moniting_and_adjusting_33" id="industrial_display_moniting_and_adjusting_33"></a>

In the v-4.3.3 version, we have provided remote monitoring for Industrial Display. The features includes (“**Luminance**”, “**Color Temperature**”, “**Contrast**”, "**Brightness" and Resolution**). for the version, **Multi-screen** (extend, clone) has been supported.

### <mark style="color:blue;">Automatic Failover Design</mark> <a href="#automatic_failover_design_36" id="automatic_failover_design_36"></a>

The stand-alone version of DeviceOn integrates all services on the same hardware device. In most situations, we can run very stably and smoothly. At the same time, we can manage thousands of devices based on different hardware specification, but we also consider and handle the abnormal, burst data into the DeviceOn server.

There is no problem to support instant data traffic in the short time. Even if the hardware load is exceeded for a long time, resulting in data loss. After the data frequency is restored to the range that the hardware can carry, the service is self-recovering under the DeviceOn design ability, no need to manually restart the repair service.

## Third-Party Updates

* OpenJRE (v1.8.0\_275)
* Tomcat (v9.0.41)
* RabbitMQ (v3.8.9), Erlang 24
* PostgreSQL (v10.15)
* MongoDB (v4.2.11)
* Grafana (v7.3.5)
