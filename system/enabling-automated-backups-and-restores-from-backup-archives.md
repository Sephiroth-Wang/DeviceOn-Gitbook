# Enabling Automated Backups and Restores from Backup Archives

This capability enables automated scheduled backups of the DeviceOn server configuration and relational databases, **excluding MongoDB sensor data repositories**, with configurable backup retention policies. The integrated migration utility facilitates restore operations in failure scenarios, restoring the system to previous known working states.

{% hint style="info" %}
1. Note that backup archives created with TPM encryption enabled during initial server deployment can only be restored to identical TPM hardware modules.
2. Additionally, restore operations are constrained to the same DeviceOn server version as the backup origination instance.
{% endhint %}

## Enable System Schedule Backups <a href="#enable-system-schedule-backups" id="enable-system-schedule-backups"></a>

1. Login to DeviceOn portal.
2. Click **System** tab in the right panel.
3. Select the tab called **System Settings** at the top of the page.
4.  Choose the item named **System Backup**\


    <figure><img src="https://hackmd.io/_uploads/SJ5SLFUba.png" alt=""><figcaption></figcaption></figure>
5.  The **system backup** feature can be enabled on the System Backup configuration page. When enabling this capability, the storage destination for backup archives must be specified. Users can configure the frequency of automated backups and the retention quantity of maintained backup archives.\


    <figure><img src="https://hackmd.io/_uploads/rymTv6Y4p.png" alt=""><figcaption></figcaption></figure>

## Performing Restore Operations from Backup Archives <a href="#performing-restore-operations-from-backup-archives" id="performing-restore-operations-from-backup-archives"></a>

Provided the backup configuration is correctly established, the system will automatically generate a backup archive with the naming convention **Backup\_YYYYMMDD\_HHMMZ.zip** saved to the designated storage location. The cadence of these backup jobs corresponds to the user-defined schedule, be that daily or monthly.



1.  Prior to initiating a system restore, the DeviceOn Server instance should be reverted to a clean baseline state. Administrators can leverage the **Reset to Default** utility to restore the system to the default configuration applied on initial software deployment.\


    <figure><img src="https://hackmd.io/_uploads/Sy1KYptNa.png" alt=""><figcaption></figcaption></figure>

Alternatively, manual **uninstallation** and **reinstallation** of the DeviceOn Server can be performed to achieve an equivalent starting state for the restore process.

2. Locate the desired backup archive within the designated storage repository and transfer it into the **DeviceOn Server** runtime environment that will serve as the restore target.
3.  Execute the **recovery.bat** script located in the **\<INSTALL\_PATH>\tools\System Recovery** directory by double-clicking the batch file.\


    <figure><img src="https://hackmd.io/_uploads/HJ0u5atNa.png" alt=""><figcaption></figcaption></figure>
4.  Follow the prompts to fill in the path of the backup file you want to restore and click **Enter**\


    <figure><img src="https://hackmd.io/_uploads/HJN4b85b6.png" alt=""><figcaption></figcaption></figure>
5.  Upon successful completion of the restore operation, the recovery script will display a “**Restore successfully**” status message.\


    <figure><img src="https://hackmd.io/_uploads/BkZW78cbT.png" alt=""><figcaption></figcaption></figure>
