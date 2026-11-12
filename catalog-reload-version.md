---

copyright:

  years: 2019, 2026
lastupdated: "2026-11-11"

keywords: private catalog, account catalogs, software, reload, version

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Reloading a software version in an {{site.data.keyword.cloud}} private catalog
{: #catalog-reload-version}

Reload a software version in your {{site.data.keyword.cloud_notm}} private catalog to update it from your source repository and restore its default imported state.
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
