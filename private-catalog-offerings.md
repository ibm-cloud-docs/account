---

copyright:
  years: 2019, 2022
lastupdated: "2022-10-26"

keywords: add software, import software, private software, add to private catalog, private catalogs, account catalogs

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}

# Adding software products to a private catalog
{: #add-software}

You can import your own private software products, such as a Terraform-based template, to be available from your private catalog for users in your account. You import the files for your product, validate that your product can be installed successfully, and then you can make it available for the users in your account with access to your private catalog.
{: shortdesc}

To start creating your own private software product for users in your account, complete the following steps:

1. Go to **Manage** > **Catalogs** in the {{site.data.keyword.cloud_notm}} console.
1. Select the row for your private catalog.
1. Click **Add** > **New offering**.
1. Enter the repository URL or TGZ archive location for your software product.
1. Click **Import**.
1. Click the **Edit offering** ![Edit offering](../icons/icon_write.svg) icon, and set at least one category for your product. This category can be used by users later to filter for the product.
1. Click **Update**.
1. From the **Configure offering** page, select the deployment target type, review the preinstallation and installation details on the **Configure offering** page, if you have any imported scripts, set the required resources if they aren't set.
1. Set the deployment values that you want to include. By default, each value that you add is displayed to the customer when they are installing your product. Include default values, if possible for each deployment value.
1. Click **Add license**, and select **Free** if you don't require a third-party license to use the software. If a license or entitlement is required, enter the information in **Third-party licenses** by clicking **Add license**.
1. Click **Edit readme** to review or update the information that is displayed for the user. The readme file information is displayed for a user when they are installing your product. Include any details that are needed for a successful installation or use of the product.
1. Click **Validate offering**, and then click **Validate**. Validation ensures that your product can be installed successfully. This step is required before you can make it available for users in your account with access to the private catalog. This can take a few minutes.
1. After your product is successfully validated, click **Publish to account** from the **Options** ![List of options icon](../icons/actions-icon-vertical.svg) menu to make it available to all users in your account through the private catalog.

Remember, your users must be assigned at least the Viewer role on the Private Catalog service to get to your product. Users with access can find it by clicking **Catalog** from the menu bar in the console, and then going to the **Private** page.
{: tip}

## Updating a published software offering
{: #update-software}

After you create and publish a software product, you can update the product if you need. You can update the name, catalog category, deployment values, and readme file information without creating a new version. When you save your changes, the product is immediately updated in the catalog.

1. Click **Manage** > **Catalogs** in the {{site.data.keyword.cloud_notm}} console, and select the row for the private catalog that contains your existing product.
1. Click the name of your product.
1. Click **Edit** from the **Options** ![List of options icon](../icons/actions-icon-vertical.svg) menu to switch your product into a draft state to update.
1. Edit the information that you want to update.
1. Click **Update** to save your changes.
1. Select **Merge changes** from the **Options** ![List of options icon](../icons/actions-icon-vertical.svg) menu to publish the updated version to your account for users to start working with immediately.

## Deprecating a published software product
{: #deprecate-software}

When you deprecate a version, all users who do not have the product that is installed no longer see it as an available option in the catalog. All customers with existing installations of the product can still access it.

To deprecate a version, complete the following steps:

1. Go to **Manage** > **Catalogs** in the {{site.data.keyword.cloud_notm}} console, and select the row for your private catalog that contains your existing product.
2. Click the name of your product.
3. Select **Deprecate** from the **Options** ![List of options icon](../icons/actions-icon-vertical.svg) menu.
4. Click **Deprecate**.

## Restoring a deprecated product
{: #restore-version}

If you deprecated a version in error, you can restore the version. However, you do need to validate the product again and merge your changes to publish it again.

1. Click **Restore** from the **Options** ![List of options icon](../icons/actions-icon-vertical.svg) menu.
2. Click **Yes** to confirm that you want to restore the deprecated version.
3. Validate your product.
4. When the product is validated, click **Merge changes** from the **Options** ![List of options icon](../icons/actions-icon-vertical.svg) menu.
5. Click **Merge**.

Merging your changes restores the version and the tile is available again from the Private page of the catalog in the console.
{: important}
