# Package and Deploy your Application

**App Store** is another powerful feature DeviceOn provides. Users can install software application onto a device remotely, or even many devices broadly. This lab guides you how to accomplish upload and wrap your application to on-premises App Store. And, after this lab, you should:

* Learn how to wrap your software for remote provisioning.
* Have the NotePad++, a popular and famous text editor, populated within the target device.

## Prerequisite <a href="#prerequisite" id="prerequisite"></a>

* A running DeviceOn server.
* A device which running on Windows operating system and installed DeviceOn Agent, that connects to DeviceOn server.
* A NotePad++ installer, 32-bit edition is recommended. Its name is “**npp.7.8.2.Installer.exe**”, something like that. It can be downloaded from [**https://notepad-plus-plus.org/downloads/**](https://notepad-plus-plus.org/downloads/).
* Automation skills to install target software package. It is because that user intervention is not possible during provisioning via App Store. For Windows it can be batch file or power shell, while for Ubuntu it may be shell scripts.

## Example

* [Notepad++ on Windows](https://eiot.blob.core.windows.net/deviceon/Material/OTA/Windows%20Npp.zip)
* [Chrome on Linux](https://eiot.blob.core.windows.net/deviceon/Material/OTA/Linux%20Google%20Chrome.zip)&#x20;
* [BIOS Update SOP](https://eiot.blob.core.windows.net/deviceon/Material/OTA/BIOS\_Update\_TOP%20SWAP.pdf)

## Step-by-Step <a href="#step-by-step" id="step-by-step"></a>

### **Step 1**: Preparation

What should we prepare for an App:

1. **Name**: The public name of app that you want to present to users.
2. **App**: App files for installing to device. There are two necessary files, installer and install script file. In windows, installer may be MSI or EXE, and install script file may be BAT. If the app need to run uninstallation, you need to prepare one more script file for uninstalling.
3. **Icon**: A well-design icon image makes app looks more professional.
4. **Description**: Detailed description text will help user knows the app more.
5. **Keywords**: Accurate keyword can lead user to the app via searching tool, making higher visibility.
6. **Category**: The same with keywords, and more. Category will directly show in app store’s first page.
7. **Provider**: The provider is company, or organization who owns the app. The same provider’s app will display together under provider’s page. Please prepare a logo image, website URL, and description about provider.
8. **Contact**: Providing contact information to users. Let user could send feedback to help app’s growth. Please prepare name of contact, and e-mail address.

{% hint style="info" %}
Note: Image specification: A squared image, in JPG, PNG, GIF formatted file. Recommendation size is 400 x 400 pixel. And smaller than 1 MB(Megabytes)
{% endhint %}

### **Step 2**: Given an App Information

<figure><img src="https://i.imgur.com/G6nUdmY.png" alt=""><figcaption></figcaption></figure>

1. **Name**: The public name of the app.
2. **Icon**: Click to upload an image as app’s icon.
3. **Is Public**: Switch to turn On/Off share property to the app. If turn On, other account can install this app to their device. If turn Off, only the account who upload this app can retrieve the app. Note: The property cannot be modified later.
4. **Description**: Text information about the app.
5. App Image: Application screenshot.
6.  **Add Keywords**: Open a dialog to set keywords. At most 10 keywords are acceptable.\


    * **Enter Keywords**: Input keywords and it will display in keyword candidate list. Manager can input a comma-separated string contains multiple keywords at once. For example: “**Editor, Text**” will be two items in keyword candidate list “**Editor**”, “**Text**”.
    * **Keyword Candidate List**: Shows extant keywords or taking apart from string input above. Click plus sign (+) in the keyword item to add to Keyword List.
    * **Keyword List**: Shows manager selected keywords. Click cross sign (x) in the keyword item to remove it from **Keyword List**.
    * Save: Save keywords in K**eyword List**.
    * **Cancel**: Discard change and close dialog.

    <figure><img src="https://i.imgur.com/UoUbuTF.png" alt=""><figcaption></figcaption></figure>
7.  **Category Name**: Select fitting category in drop-down list.

    * **Category List**: Selected category list. Click cross sign (x) in the category item to remove it from Category List.
    * **Open**: Open Category Candidate List.
    * **Search**: Enter keyword to filter matching category in Category Candidate List.
    * **Category Candidate List**: All categories list, click on suitable category to add to Category List

    <figure><img src="https://i.imgur.com/xTZNFwb.png" alt=""><figcaption></figcaption></figure>
8.  **Add Provider**: If provider not found in provider list, manager can add one here.\


    * **Logo**: Upload an image as company’s logo.
    * **Company** Name: The name of company
    * **Company** Website: URL of website.
    * **Company** Bio: Text description of company.
    * **CONFIRM**: Save to database and can be found in Select Provider.
    * **CANCEL**: Discard change and close dialog.

    <figure><img src="https://i.imgur.com/Vrztixo.png" alt=""><figcaption></figcaption></figure>
9. **Select Provider**: Select a provider in extant provider list.
10. **Add Contact**: If contact not found in contact list, manager can add one here.\


    * **CANCEL**: Discard change and close dialog.
    * **Contact Name**: Name of contact.
    * **Contact Email**: Email of contact.
    * **CONFIRM**: Save to database and can be found in Select Contact.
    * **CANCEL**: Discard change and close dialog.

    <figure><img src="https://i.imgur.com/Fm6E5Mv.png" alt=""><figcaption></figcaption></figure>
11. **Contact Support**: Select a contact in extant contact list.
12. **Next**: To next step.

The result similar as below sample of step 1.\


<figure><img src="https://i.imgur.com/HW7hHhZ.png" alt=""><figcaption></figcaption></figure>

### **Step 3**: Upload your App

<figure><img src="https://i.imgur.com/DdRwj5u.png" alt=""><figcaption></figcaption></figure>

1. **Version**: App’s version number. 3 or 4 digits and separated by dot(.). For example: 1.0.0 or 1.2.3.4
2. **Operating System**: Select OS of the app can install. Multiple OS are acceptable.
3. **Save to**: Select an option where app package file will save after Step 3. Confirm. \[Local] means there will be two zip files download to your local machine, please save it properly, and uploading to specific repository by Upload App from \[Repository Name] means Online Wrap Tool will upload app package files to the repository directly.
4. **Select Directory**: Select a directory to upload, which contains files are necessary for installing the app.
5. **Install Script**: Select a runnable script file for executing installation, and the script file must return “0”, do not launch the GUI application as possible.
6. **Uninstall Option**: Switch On/Off to determine this version’s app can uninstall or not.
7. **Uninstall Script**: Select a runnable script file for executing uninstallation.
8. **Advanced Option**: Switch On/Off to show/hide more option.
9. **Reboot Option**: Switch On/Off to determine this version’s app need reboot after installation or not.
10. **Result Script**: Select a runnable script file for executing checking result of installation is successful or failed. The script file must return “0”, that means success, and all other value will be took as fail.
11. **Back**: Back to previous step.
12. **Next**: To next step.\


    <figure><img src="https://i.imgur.com/39Djo2w.png" alt=""><figcaption></figcaption></figure>

### Step 4: Confirm

1. App Information/Content: Display all data entered in previous steps, please check again before you click Confirm.
2. Back: Back to previous step.
3. Confirm: After checking App Information/Content, click Confirm to finish this tool.

<figure><img src="https://i.imgur.com/1gtdbRZ.png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Note: Depending on selected option of Step 3: Save To, you will save two zip files or waiting a while for uploading app package files.
{% endhint %}

