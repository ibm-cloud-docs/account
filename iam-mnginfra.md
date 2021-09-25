---

copyright:

  years: 2017, 2020

lastupdated: "2020-09-22"


keywords: classic infrastructure access, VPN subnet access, classic infrastructure permissions, device access

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:deprecated: .deprecated}

# Managing classic infrastructure access
{: #mngclassicinfra}

You can update permissions for classic infrastructure services or add device and VPN subnet access for a user at any time. To access the classic infrastructure permissions, go to **Manage** &gt; **Access (IAM)** in the console, select **Users**. Then, select the user's name that you want to update access for, and click **Classic infrastructure**.
{: shortdesc}

You must be assigned the Manage users classic infrastructure permission and be an ancestor of the user within the classic infrastructure user hierarchy. Account owners have full access to the account, so they do not see the permissions on the page. Individual users can't edit their own permissions, and they also don't see permissions on the page.

When a classic infrastructure user invites another user to the account, the classic infrastructure user becomes the parent user. When a child of a parent invites other users to the account, those users become descendants of the original parent, who is now considered their ancestor.
{: note}

Support center account management access is recommended for users that are working with classic infrastructure resources. To perform many tasks with classic infrastructure resources, such as creating or deleting a virtual server instance, users must have access to work with support cases. For more information about assigning this type of access, see [Assigning access to account management services](/docs/account?topic=account-account-services).

1. Select **Permissions** to update the user's permissions. You can select from four types of permissions: account, devices, network, and services. Individually select permissions from each category, or use a permission set option to assign permissions in bulk. For more information, see [Classic infrastructure permissions](https://cloud.ibm.com/docs/account?topic=account-infrapermission).

   The account management and support permissions that you previously assigned to users in your account are now migrated from classic infrastructure permissions to migrated IAM access groups. For more information, see [Migrated SoftLayer account permissions](/docs/account?topic=account-migrated_permissions).

2. To grant a user device access, select **Devices**, and assign the access to specific devices and device types as needed.

   Access to devices is assigned after the user is invited to the account. The device permissions apply to the specific devices that are assigned for the user. You can select specific devices from the list, or you can assign access by device type. If you assign access by device type, you might want to use the **Enable future access** options to ensure that each time new devices of a specific type are added, the user automatically gets assigned access to those devices.

3. To update a user's access to VPN subnets, select **VPN subnets**. You must have the following type of access to assign VPN access:

   * To update your own access, you must have the VPN Administration permission or be the master user.
   * To update a user to which you are a parent, you must have the VPN Administration permission.
   * To update any user's access, you must have the VPN Administration permission and an IAM policy on the User management service with Viewer role or higher assigned or be the master user.


Use the **Auto-assign** option to set how the user gets access to VPN subnets based on their device access. If this option is set to on, the user is automatically assigned access to all subnets for the devices they already have access to. You can set this option to off to manually select subnets from the list.
    
You can define the type of VPN subnets that the user has access to by using the **VPN type** option. If you select **None**, no VPN access can be assigned. If you have the correct access, you can define the type of VPN subnets that the user has access to by using the VPN type option. If you select None, no VPN access can be assigned. 
