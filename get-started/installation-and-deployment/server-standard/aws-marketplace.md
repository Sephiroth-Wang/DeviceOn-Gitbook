# AWS Marketplace

## Step 1: Deploy DeviceOn from AWS Marketplace

> Please enter to [AWS Marketplace](https://aws.amazon.com/marketplace/pp/B08972SVHN) and click on the “**Continue to Subscribe**”

![](https://i.imgur.com/OVj1tMU.png)

> Sign in your AWS account.

![](https://i.imgur.com/UBJvjgx.png)

> Click on the “**Continue to Configuration**”

![](https://i.imgur.com/aaTNrmc.png)

> Congigure this DeviceOn software and click on the “**Continue to Launch**”

1. Deleviery Method: **64-bit (x86) Amazon Machine Image (AMI)**
2. Software Version: **4.2.3 (May, 22, 2020)**
3. Region: Select the Region that the nearest to your location.

![](https://i.imgur.com/fs1zc0o.png)

> Launch this DeviceOn software

1. Choose Action: **Launch from Website**
2. EC2 Instance Type: **t2.large** (Recommand select higher than t2.large for better performance.)
3. VPC Settings: **default vpc**
4. Subnet Settings: **default subnet**

![](https://i.imgur.com/EatuBTI.png)

5. Security Group Settings:

> Create a security group based on our setting, enter name, description of this security group.

![](https://i.imgur.com/DCWfS7W.png)

![](https://i.imgur.com/apGQIDK.png)

6. Key Pair Settings

> Create a key pair in EC2, enter name and select file format as “**pem**”. The key pair used to get the password of Remote Desktop.

![](https://i.imgur.com/lCtEn93.png)

![](https://i.imgur.com/VcHMx16.png)

![](https://i.imgur.com/7WRCvS6.png)

![](https://i.imgur.com/FecVIeA.png)

7. Click on the “**Launch**” to deploy EC2 machine.

![](https://i.imgur.com/igQQkFP.png)

## Step 2: Login EC2 Virtual Machine

> After deployment, please enter to AWS EC2 Console, select your instance and get the connect remote desktop and password.

![](https://i.imgur.com/xeywwYf.png)

![](https://i.imgur.com/oSVchZB.png)

> In order to retrieve your password you will need to specify the path of this **Key Pair (DeviceOnKey.pem)** on your machine.

![](https://i.imgur.com/E8fmZt3.png)

> There is a **Quick Start Guide** on the desktop and include the random password to access DeviceOn Web Service.

![](https://i.imgur.com/EtVnq9O.png)

![](https://i.imgur.com/ARMqoHI.png)

## Step 3: Login DeviceOn Web Service

> Enter to DeviceOn main page (Suggest using Microsoft Edge or Google Chrome for best experience), please follow the steps to finish the basic questionnaire and then confirm the related policy and agreement. (As below pictures)

![](https://i.imgur.com/vy4VZtw.png)

![](https://i.imgur.com/LDKhjNd.png)

> Enter the default account and password (through **Quick Start Guide**)

* Account: [root@advantech.com.tw](mailto:root@advantech.com.tw)
* Password: \*\*\*\*\*\*\*\*

{% hint style="info" %}
**Please remember to modify your own password after log-in.**
{% endhint %}

![](https://i.imgur.com/9Rceh6F.png)
