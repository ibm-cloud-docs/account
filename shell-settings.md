---

copyright:
  years: 2020
lastupdated: "2020-09-18"

keywords: cloud shell settings, cloud shell service, enable cloud shell, disable cloud shell, cloud shell locations, cloud shell access, cloud shell iam, cloud shell role, cloud shell administrator, cloud shell service

subcollection: cloud-shell

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:important: .important}
{:note: .note}
{:support: data-reuse='support'}
{:external: target="_blank" .external}

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
3. On the individual user's page, click the **Access policies** tab, and then click **Assign access**.
4. On the Assign access page, select **Account management**.
5. For the type of access, select **{{site.data.keyword.cloud-shell_notm}}**.
6. Select **Administrator**, and then click **Add**.
7. In the Access summary pane, click **Assign**.

For more information, see the IAM roles and actions for the [{{site.data.keyword.cloud-shell_notm}}](/docs/account?topic=account-account-services#shell-service-acct-mgmt) account management service.

## Enabling or disabling {{site.data.keyword.cloud-shell_short}} for an account
{: #shell-settings-enable}


By default, {{site.data.keyword.cloud-shell_short}} is enabled for an account. As an account owner or user with the correct access, you can enable or disable {{site.data.keyword.cloud-shell_short}} for users in the account.

When the {{site.data.keyword.cloud-shell_short}} availability setting is enabled, {{site.data.keyword.cloud-shell_short}} is available to all users in the account. If the setting is disabled, all users in the account are denied access to {{site.data.keyword.cloud-shell_short}}. 

To enable or disable {{site.data.keyword.cloud-shell_short}} for the account, complete the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, go to **Manage** > **Account**, and select **IBM {{site.data.keyword.cloud-shell_short}} settings**.
2. Select the **Enabled** or **Disabled** toggle, and then click **Save changes**.

## Selecting {{site.data.keyword.cloud-shell_short}} locations for an account
{: #shell-settings-locations}

By default, all locations for the account are enabled to store user session data, and the nearest available location is chosen. Users are routed to the nearest available location, such as Dallas (us-south), Frankfurt (eu-de), or Tokyo (jp-tok).

As an account owner or user with the correct access, you can select whether {{site.data.keyword.cloud-shell_short}} is enabled to store data only in specific locations for the account. To select {{site.data.keyword.cloud-shell_short}} locations for the account, complete the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, go to **Manage** > **Account**, and select **IBM {{site.data.keyword.cloud-shell_short}} settings**.
2. Ensure that {{site.data.keyword.cloud-shell_short}} Availability is enabled.
3. Select the toggle for each location that you want to enable or disable for the account.
4. Optional: Select **Enable new locations by default** to automatically allow {{site.data.keyword.cloud-shell_short}} user session data to be stored in new locations when they are available. If this option is not selected, you must select the toggle for each new location that you want to enable as it becomes available.
5. Click **Save changes**.
