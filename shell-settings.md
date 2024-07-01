---

copyright:
  years: 2020, 2024
lastupdated: "2024-03-28"

keywords: cloud shell settings, cloud shell service, enable cloud shell, disable cloud shell, cloud shell locations, cloud shell access, cloud shell iam, cloud shell role, cloud shell administrator, cloud shell service

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Updating {{site.data.keyword.cloud-shell_short}} settings
{: #shell-settings}

{{site.data.keyword.cloud-shell_full}} settings are managed in the {{site.data.keyword.cloud}} console. As an account owner or {{site.data.keyword.cloud-shell_short}} administrator, you can control whether users in an account can access {{site.data.keyword.cloud-shell_short}}, and you can select the location availability for an account.
{: shortdesc}

{{site.data.keyword.cloud-shell_notm}} is a cloud-based shell workspace that you can access through your browser. {{site.data.keyword.cloud-shell_short}} is preconfigured with the full {{site.data.keyword.cloud_notm}} CLI, plug-ins, and tools that you can use to manage apps, resources, and infrastructure. For more information, see [Getting started with {{site.data.keyword.cloud-shell_notm}}](/docs/cloud-shell?topic=cloud-shell-getting-started).

## Before you begin
{: #shell-settings-admin}

Only account owners, users assigned the Administrator role for the {{site.data.keyword.cloud-shell_short}} account management service, or users assigned the Administrator role on all account management services can change the {{site.data.keyword.cloud-shell_short}} settings. To assign this access to a user in your account, complete the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, go to **Manage** > **Access (IAM)**, and select **Users**.
2. On the Users page, select the user that you want to assign the role to.
3. On the individual user's page, click the **Access** tab, and then click **Assign access**.
4. Select the service **{{site.data.keyword.cloud-shell_notm}}**.
5. For the role, select **Administrator**, and then click **Review**. For more information, see [IAM roles](/docs/account?topic=account-userroles#iamusermanrol).
6. Click **Add** to add your policy configuration to your policy summary.
7. Click **Assign**.

For more information, see the IAM roles and actions for the [{{site.data.keyword.cloud-shell_notm}}](/docs/account?topic=account-account-services&interface=ui#account-management-actions-roles) account management service.

## Enabling or disabling {{site.data.keyword.cloud-shell_short}} for an account
{: #shell-settings-enable}

By default, {{site.data.keyword.cloud-shell_short}} is enabled for an account. As an account owner or user with the correct access, you can enable or disable {{site.data.keyword.cloud-shell_short}} for users in the account.

When the {{site.data.keyword.cloud-shell_short}} availability setting is enabled, {{site.data.keyword.cloud-shell_short}} is available to all users in the account. If the setting is disabled, no users in the account can access {{site.data.keyword.cloud-shell_short}}. The **{{site.data.keyword.cloud-shell_notm}}** icon ![{{site.data.keyword.cloud-shell_notm}} icon](../icons/terminal-cloud-shell.svg "IBM Cloud Shell") is disabled in the {{site.data.keyword.cloud_notm}} console.

To enable or disable {{site.data.keyword.cloud-shell_short}} for the account, complete the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, go to **Manage** > **Account**, and select **IBM {{site.data.keyword.cloud-shell_short}} settings**.
2. Select the **Enabled** or **Disabled** toggle, and then click **Save changes**.

## Enabling or disabling {{site.data.keyword.cloud-shell_short}} locations for an account
{: #shell-settings-locations}

The Tokyo region for {{site.data.keyword.cloud-shell_short}} is deprecated and will no longer be supported by {{site.data.keyword.cloud-shell_short}} as of 2 July 2024. For more information, see the [release notes](/docs/cloud-shell?topic=cloud-shell-release-notes#cloud-shell-mar2824).
{: deprecated}

By default, all locations for the account are enabled, and the nearest available location is selected. Users are routed to the nearest available location, such as Dallas (us-south), Frankfurt (eu-de), or Tokyo (jp-tok).

As an account owner or user with the correct access, you can select whether {{site.data.keyword.cloud-shell_short}} is enabled only in specific locations for the account. To select {{site.data.keyword.cloud-shell_short}} locations for the account, complete the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, go to **Manage** > **Account**, and select **IBM {{site.data.keyword.cloud-shell_short}} settings**.
2. Ensure that {{site.data.keyword.cloud-shell_short}} Availability is enabled.
3. Select the toggle for each location that you want to enable or disable for the account.
4. Optional: Select **Enable new locations by default** to automatically enable new locations when they are available. If this option is not selected, you must select the toggle for each new location that you want to enable as it becomes available.
5. Click **Save changes**.

## Enabling or disabling {{site.data.keyword.cloud-shell_short}} features for an account
{: #shell-features-enable}

Account owners or users with {{site.data.keyword.cloud-shell_short}} administrator access can enable or disable {{site.data.keyword.cloud-shell_short}} features for an account. By default, all features for the account are enabled. The feature settings apply only to the enabled {{site.data.keyword.cloud-shell_short}} locations.

To enable or disable {{site.data.keyword.cloud-shell_short}} features for the account, complete the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, go to **Manage** > **Account**, and select **IBM {{site.data.keyword.cloud-shell_short}} settings**.
2. Select the toggle for the feature that you want to enable or disable for the account. For example, **File upload and download** and **Web preview**.
3. Optional: Select **Enable new features by default** to automatically allow new features to be enabled for the account when they are available. If this option is not selected, you must select the toggle for each new feature that you want to enable as it becomes available.
4. Click **Save changes**.

## Assigning access to {{site.data.keyword.cloud-shell_short}} and its features at a user level
{: #shell-access-user}

An account administrator can grant specific users access to {{site.data.keyword.cloud-shell_short}} and its features, such as **File upload and download** and **Web preview**, even if {{site.data.keyword.cloud-shell_short}} settings are disabled at the account level.

The IAM policy can be applied to specific locations with different roles. The roles are used to control the access of specific {{site.data.keyword.cloud-shell_short}} features.

The IAM policy takes priority and is active only if the {{site.data.keyword.cloud-shell_short}} account setting is disabled. If the {{site.data.keyword.cloud-shell_short}} account setting is enabled and the IAM policy is set, the IAM policy has no effect. In that scenario, all users in account can access {{site.data.keyword.cloud-shell_short}}.

To assign {{site.data.keyword.cloud-shell_short}} access to a particular user, complete the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, go to **Manage** > **Access (IAM)**, and select **Users**.
2. On the Users page, select the user that you want to assign the role to.
3. On the individual user's page, click the **Access polcies** tab, and then click **Assign access**.
4. For the service, select **{{site.data.keyword.cloud-shell_notm}}**. Then, click **Next**.
5. Scope the access to **Specific resources**. Select a location to enable the features in. Then, click **Next**.
6. Select one or more roles to assign to the user. For example, if you want to enable the **File Upload** and **File Download** features for the user, select the **File Manager** role. For more information, see [IAM roles](/docs/account?topic=account-userroles#iamusermanrol).
7. Click **Review**.
8. Click **Add** to add your policy configuration to your policy summary.
9. Click **Assign**.

When the user logs in to their {{site.data.keyword.cloud_notm}} account, the user now has access to {{site.data.keyword.cloud-shell_short}} and the file management features within {{site.data.keyword.cloud-shell_short}}.
