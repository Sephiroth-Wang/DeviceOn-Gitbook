# Azure Marketplace

## Step 1: Deploy DeviceOn from Azure Marketplace

> Please enter to [Azure Marketplace](https://azuremarketplace.microsoft.com/en-us/marketplace/apps/advantech.deviecon\_on\_windows\_vm\_v1?tab=Overview) and click “GET IT NOW”

![](https://i.imgur.com/n2cx2uY.png)

> Sign in your Account

![](https://i.imgur.com/V62g7X9.png)

> You will enter to Azure portal and please click on **Start with pre-set configuration** to be quick deployment

![](https://i.imgur.com/JSYtv3q.png)

> This page includes our recommended configuration for DeviceOn Server, you can just click on **Continue to create VM**, following the default setting.

![](https://i.imgur.com/u8mlMGw.png)

> In this page, please note that the red star parts info are MUST.

* Select your Azure Subscription
* Create a new resource group or pick-up
* Define your Virtual Machine name
* Select the Virtual Machine region, you can pick one which is the nearest one to your location
* Select **DeviceOn** as default Image
* Here you need to create the **Username** and remember the **Password** which is to secure this DeviceOn VM (**Remote Desktop Used**)

> Then click Next to move on, or you can directly click “Review + Create”, then all the following items will be set as default.

![](https://i.imgur.com/OXlbgE9.png)

> By using the default disk Premium SSD, then click **Next** to move on.

![](https://i.imgur.com/McaKkY1.png)

> Set the network interface

* Select the one you just defined in previous grouping or create new

![](https://i.imgur.com/2YOJwUh.png)

> In this page, you can schedule the power management of VM for reducing the unnecessary cost

* Auto shut-down schedule (please make sure the time zone is correct)
* Email account

![](https://i.imgur.com/BvBqxRe.png)

> Basically, you can click **Review + Create** if you don’t need advanced setting. VM will be validating and creating within 5 minutes.

![](https://i.imgur.com/eL2Hn47.png)

> A few minutes later, you can see below picture that VM has been created.

\


<figure><img src="https://i.imgur.com/VAExuMR.png" alt=""><figcaption></figcaption></figure>

<figure><img src="https://i.imgur.com/08dKVNf.png" alt=""><figcaption></figcaption></figure>

> Click “Go to resource” to review more detail.

![](https://i.imgur.com/zSN699M.png)

> After deployment, please click on “**Connect**” to remote login to VM via Microsoft Remote Desktop. The password that you configure on Step 1. There is a **Quick Start Guide** on the desktop and include the random password to access DeviceOn Web Service.

![](https://i.imgur.com/3du0D3U.png)

![](https://i.imgur.com/vsa89oo.png)

## Step 2: Access DeviceOn Web Service

> Please copy the public address first from Azure VM, and open Microsoft Edge or other browsers to paste the IP address (Suggest using Microsoft Edge for best experience)

![](https://i.imgur.com/jWU2qjK.png)

![](https://i.imgur.com/kigRxPW.png)

> Enter to DeviceOn main page, please follow the steps to finish the basic questionnaire and then confirm the related policy and agreement. (As below pictures)

![](https://i.imgur.com/BwrgUsw.png)

![](https://i.imgur.com/3nGwybM.png)

> Enter the default account and password (through **Quick Start Guide**)

* Account: [root@advantech.com.tw](mailto:root@advantech.com.tw)
* Password: \*\*\*\*\*\*\*\*

_Note: Please remember to modify your own password after log-in._

![](https://i.imgur.com/FVuGMo5.png)
