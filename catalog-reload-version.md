---

copyright:

  years: 2019, 2025
lastupdated: "2025-01-28"

keywords: private catalog, account catalogs, software, reload, version

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Reloading a software version
{: #catalog-reload-version}

You can reload a version of software in your private catalog to update the version based on your current repository. When you reload a version, you revert it to its default state when you first imported the software. 
{: shortdesc}

## Reloading an unpublished version
{: #catalog-reload-unpublished}

To update an unpublished version of software, you must reload the version from your source repository and validate it.  

1. In the {{site.data.keyword.cloud}} console, click **Manage** > **Catalogs** > **Private catalogs**. 
1. Select the private catalog where your product is located. 
1. Select your product. 
1. Select the version of the software that you want to reload.
1. Open the **Actions** menu, and select **Reload version**.
1. Click **Reload version**. 
1. Configure and validate your software. 

   The configuration and validation steps vary based on the deployment method. 
   {: note}

## Reloading a published version
{: #catalog-reload-published}

To update a published version of your software, you must create a draft, reload the version from your source repository, validate, and merge the changes.  

1. In the {{site.data.keyword.cloud_notm}} console, click **Manage** > **Catalogs** > **Private catalogs**. 
1. Select the private catalog where your product is located. 
1. Select your product. 
1. Select the version of the software that you want to reload. 
1. Open the **Actions** menu, and select **Edit** to create a draft of your original version.
1. In the draft version, open the **Actions** menu, and select **Reload version**.
1. In the Reload version panel, click **Reload version**. 
1. Configure and validate your software. 

   The configuration and validation steps vary based on the deployment method.
   {: note}

1. Open the **Actions** menu, and select **Merge changes**.
1. Click **Merge** to update your original version.
