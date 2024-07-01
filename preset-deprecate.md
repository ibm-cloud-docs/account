---

copyright:
  years: 2022
lastupdated: "2022-12-06"

keywords: deprecate object, restore object, catalog, catalogs, objects, private catalog, preset configuration, deprecate preset, preset, restore preset configuration

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}


# Deprecating, restoring, and deleting your preset configurations
{: #dep-restore-presets}

If you want to stop the use of one of your preset configurations, you can deprecate that object. If a preset configuration is deprecated, instances and users on the account are still able to use it for 60 days, and after that the preset configuration is deleted. Also, when the preset configuratio is deprecated, no new instances or users can be added to it. When the preset configuration is deleted, it's permanently removed from your private catalog.
{: shortdesc}

## Before you begin
{: #prereq-dep-restore-presets}

You need to be assigned the editor role on the catalog management service. For more information, see [Assigning users access](/docs/account?topic=account-catalog-access).

   If you don't see what you're expecting in the console based on your permissions, try refreshing your session by going to https://cloud.ibm.com/login.
   {: tip}

## Deprecating your preset configuration
{: #deprecate-preset}
{: ui}

If your preset configuration is published or shared and is associated with instances, then you need to deprecate it before it can be deleted. After you deprecate, instances continue to have access to the preset configuration for 60 days. Users and instances can't be added to the preset configuration during this time. You also have 60 days to restore the preset configuration from deprecation.

To deprecate your preset configuration, use the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, go to **Manage** > **Catalogs**, select **Objects**.
1. Select your preset configuration.
1. Click **Actions** and select **Deprecate object**.

## Restore the deprecated preset configuration by using the console
{: #restore-preset}
{: ui}

When you restore a deprecated preset configuration, you are required to validate and publish the preset configuration again.

To restore your preset configuration, use the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, go to **Manage** > **Catalogs**, select **Objects**.
1. Select your preset configuration.
1. Click **Actions** and select **Restore object**.

## Deleting your preset configuration
{: #delete-preset}
{: ui}

If your preset configuration is not published, or if your preset configuration is published but it's not associated with instances, you can delete your preset configuration. Deleted preset configurations are permanently removed from your private catalog and can't be restored.

To delete your preset configuration, use the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, go to **Manage** > **Catalogs**, select **Objects**.
1. Select your preset configuration.
1. Click **Actions** and select **Delete object**.

## Deprecate a preset configuratio by using the CLI
{: #deprecate-cicd-preset}
{: cli}

If your preset configuration is published or shared and is associated with instances, then you need to deprecate it before it can be deleted. After you deprecate, instances continue to have access to the preset configuration for 60 days. Users and instances can't be added to the preset configuratio during this time. You also have 60 days to restore the preset configuration from deprecation.

To deprecate your preset configuration, use the following steps:

1. Deprecate the existing preset configuration.
    ```bash
    ibmcloud catalog offering deprecate --version-locator <VERSION_LOCATOR>
    ```
    {: codeblock}


## Restore a deprecated preset configuration by using the CLI
{: #restore-cicd-preset}
{: cli}

When you restore a deprecated preset configuration, you are required to validate and publish the preset configuration again.

1. Restore the deprecated preset configuration. This action creates a draft version.
    ```bash
    ibmcloud catalog offering restore --version-locator <VERSION_LOCATOR>
    ```
    {: codeblock}

## Deleting your preset configuration by using the CLI
{: #delete-preset-cli}
{: cli}

If your preset configuration is not published, or if your preset configuration is published but it's not associated with instances, you can delete your preset configuration. Deleted preset configurations are permanently removed from your private catalog and can't be restored.

To delete your preset configuration, use the following steps:

1. Delete your preset configuration.
    ```bash
    ibmcloud catalog object delete [--catalog CATALOG] [--name NAME]
    ```
    {: codeblock}

    For more information on this command, enter:
    ```bash
    ibmcloud catalog object help delete
    ```
    {: codeblock}
