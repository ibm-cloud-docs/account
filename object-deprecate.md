---

copyright:
  years: 2020, 2022
lastupdated: "2022-12-06"

keywords: deprecate object, restore object, catalog, catalogs, objects, private catalog, vpe object, deprecate vpe, restore vpe, vpe

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}


# Deprecating, restoring, and deleting your Virtual Private Endpoints
{: #dep-restore-objects}

If you want to stop the use of one of your VPEs, you can deprecate that object. If a VPE is deprecated, instances and users on the account are still able to use it for 60 days, and after that the VPE is deleted. Also, when the VPE is deprecated, no new instances or users can be added to it. When the VPE is deleted, it's permanently removed from your private catalog.
{: shortdesc}

## Before you begin
{: #prereq-dep-restore-object}

You need to be assigned the editor role on the catalog management service. For more information, see [Assigning users access](/docs/account?topic=account-catalog-access).

   If you don't see what you're expecting in the console based on your permissions, try refreshing your session by going to https://cloud.ibm.com/login.
   {: tip}

## Deprecating your VPE
{: #deprecate-object}
{: ui}

If your VPE is published or shared and is associated with instances, then you need to deprecate it before it can be deleted. After you deprecate, instances continue to have access to the VPE for 60 days. Users and instances can't be added to the VPE during this time. You also have 60 days to restore the VPE from deprecation.

To deprecate your VPE, use the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, go to **Manage** > **Catalogs**, select **Objects**.
1. Select your VPE.
1. Click **Actions** and select **Deprecate object**.


## Restore the deprecated version by using the console
{: #restore-object}
{: ui}

When you restore a deprecated VPE, you are required to validate and publish the object again.

To restore your VPE, use the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, go to **Manage** > **Catalogs**, select **Objects**.
1. Select your VPE.
1. Click **Actions** and select **Restore object**.


## Deleting your VPE
{: #delete-object-ui}
{: ui}

If your VPE is not published, or if your VPE is published but it's not associated with instances, you can delete your VPE. Deleted VPEs are permanently removed from your private catalog and can't be restored.

To delete your VPE, use the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, go to **Manage** > **Catalogs**, select **Objects**.
1. Select your VPE.
1. Click **Actions** and select **Delete object**.

## Deprecate a VPE by using the CLI
{: #deprecate-cicd-object}
{: cli}

If your VPE is published or shared and is associated with instances, then you need to deprecate it before it can be deleted. After you deprecate, instances continue to have access to the VPE for 60 days. Users and instances can't be added to the VPE during this time. You also have 60 days to restore the object from deprecation.

To deprecate your VPE, use the following steps:

1. Deprecate the existing VPE.
    ```bash
    ibmcloud catalog offering deprecate --version-locator <VERSION_LOCATOR>
    ```
    {: codeblock}


## Restore a deprecated VPE by using the CLI
{: #restore-cicd-object}
{: cli}

When you restore a deprecated version, you are required to validate and publish the VPE again.

1. Restore the deprecated VPE. This action creates a draft version.
    ```bash
    ibmcloud catalog offering restore --version-locator <VERSION_LOCATOR>
    ```
    {: codeblock}

## Deleting your VPE by using the CLI
{: #delete-object-cli}
{: cli}

If your VPE is not published, or if your VPE is published but it's not associated with instances, you can delete your VPE. Deleted VPEs are permanently removed from your private catalog and can't be restored.

To delete your VPE, use the following steps:

1. Delete your VPE.
    ```bash
    ibmcloud catalog object delete [--catalog CATALOG] [--name NAME]
    ```
    {: codeblock}

    For more information on this command, enter:
    ```bash
    ibmcloud catalog object help delete
    ```
    {: codeblock}
