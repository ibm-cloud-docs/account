---

copyright:

  years: 2017, 2021

lastupdated: "2021-09-07"

keywords: SoftLayer permissions, classic infrastructure access, classic infrastructure permission, migrated SoftLayer permissions, migrated permission access group

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:important: .important}
{:tip: .tip}

# Classic infrastructure permissions
{: #infrapermission}

When you invite a user to your account, you can select from three classic infrastructure permission sets that assign bulk access: View only, Basic user, Super user.
{:shortdesc}

When you invite someone to the account, only you, the account owner, or a user with the Manage user classic infrastructure permission, can adjust the permissions for the user. You can assign only the level of permissions or a subset of the permission that you're already assigned, if you're not the account owner. An account owner can update anyone's permissions in the account to have any level of access.

Extra permissions can be set after the user accepts the invitation. For example, the initial permission set assigned on the invitation doesn't grant access to devices. So, you must grant device access after the user accepts the invitation. For more information, see [Managing classic infrastructure access](/docs/account?topic=account-mngclassicinfra).

Support center account management access is recommended for users working with classic infrastructure resources. To perform many tasks when working with classic infrastructure resources, such as creating or deleting a virtual server instance, users must have access to work with support cases. For more information about assigning this type of access, see [Assigning access to account management services](/docs/account?topic=account-account-services).
{: tip}

The following graphic shows how classic infrastructure permissions are assigned per user. You can grant each user access to a classic infrastructure service or device by selecting from the granular permission options to customize each user's access.

![Classic infrastructure access](images/ClassicIaaS.svg "Assigning classic infrastructure access by selecting a user, device, or service, then any combination of granular permissions"){: caption="Figure 1. Assigning classic infrastructure access by selecting a user, device, or service, then any combination of granular permissions" caption-side="bottom"}

There are four main categories of permissions to choose from: account, devices, network, and services. The following lists provide examples from each category highlighting some of the commonly assigned permissions from each. To view all of the available permissions from each category, go to **Manage** > **Access (IAM)** > **Users**. Then, select a user's name from the list that you can manage access for, then click **Classic infrastructure**. 

**Account**
- Add and upgrade storage
- Manage users
- Add and upgrade services
- Add server

**Devices**
- Upgrade server
- Manage load balancers
- Manage Firewalls 

**Network**
- Add IP addresses
- VPN administration 
- Network gateways
- Security groups

**Services**
- Upgrade services
- Manage DNS
- Manage SSH keys
- Manage certificates

## Migrated classic infrastructure permissions
{: #predefined}

A set of classic infrastructure permissions for viewing and managing billing information and working with support cases are now migrated to access groups. The users in your account who were previously assigned these permissions are now assigned to the respective migrated permission access group. As a result, the classic infrastructure permissions can be directly managed by using IAM access policies. For more information about the migrated permissions and the access groups that are used for each, see [Managing migrated SoftLayer account permissions](/docs/account?topic=account-migrated_permissions).
