# Visualize Device Data through Grafana Dashboards

{% hint style="info" %}
Grafana is an open-source software for monitoring and analysis. One of its major characteristics is it supports many different data sources, from popular CloudWatch, Elasticsearch, Graphite, and influxDB, to OpenStack Gnocchi or Google Calendar. Its range is very extensive. However, for other data source require to implement SimpleJson to access your data. The DeviceOn native support SimpleJson APIs and data source plugin on Grafana. This lab guides you how to visualize device data via Grafana dashboard.
{% endhint %}

## Prerequisite <a href="#prerequisite" id="prerequisite"></a>

* A running DeviceOn server.
* A running Grafana service with DeviceOn data source plugin.
* A device which installed WISE-Agent, that connects to DeviceOn server.

## Steps to Visualization <a href="#step-by-step" id="step-by-step"></a>

*   **Step 1**: Launch Grafana Web Service Shortcut on Desktop or access the Grafana service endpoint.\


    <figure><img src="https://i.imgur.com/TVKIcMC.png" alt=""><figcaption></figcaption></figure>
*   **Step 2**: Login to Grafana portal with your account, password (Default: **admin**/**admin**)\


    <figure><img src="https://i.imgur.com/GN1Mt2C.png" alt=""><figcaption></figcaption></figure>
*   **Step 3**: Create a data source to access DeviceOn SimpleJson API.\


    Click on “**Add data source**” and select “**DeviceOn-SimpleJson**”, (for previous version might be RMM-SimpleJson)

![](https://i.imgur.com/VUmUiyw.png)

<figure><img src="https://i.imgur.com/5BGlhm5.png" alt=""><figcaption></figcaption></figure>

<figure><img src="https://i.imgur.com/EnZ55ZG.png" alt=""><figcaption></figcaption></figure>

*   **Step 4**: Given below parameters for data source plugin to retrieve device data from DeviceOn APIs.

    * **URL**: http://\<DEVICEON\_SERVER>:8080/rmm/v1/grafana/simplejson
    * **Access**: Browser
    * **Auth**: Basic Auth (Support on perpetual version)
    * **Basic Auth**: DeviceOn Account & Password

    ![](https://i.imgur.com/7FDDHYC.png)
* **Step 5**: Create a dashboard to visualize your device data.

<figure><img src="https://i.imgur.com/xqSv2SV.png" alt=""><figcaption></figcaption></figure>

Select “Add Query” for your device.

<figure><img src="https://i.imgur.com/AoRK8iH.png" alt=""><figcaption></figcaption></figure>

Select DeviceOn-SimpleJson from “Queries to”, and pick-up your device with AgentID, Plugin, Sensor and Alias Name (Option).

<figure><img src="https://i.imgur.com/oKKbtRM.png" alt=""><figcaption></figcaption></figure>
