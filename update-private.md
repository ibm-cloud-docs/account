---

copyright:
  years: 2020
lastupdated: "2020-04-02"

keywords: catalog, private catalog, update, private catalog product, update version

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:new_window: target="_blank"}

# Updating a software version
{: #update-private}

In this tutorial, you update the version of the installed apache-two-instances product. 
{: shortdesc}

## Before you begin
{: #prereq-update}

To complete this tutorial, you need to be assigned the editor role on the catalog management service. With this type of access, you can create private catalogs and set filters that apply only to users with access to your private catalog. You can also view the account-level filters on the Settings page, but you can't update them. For more information, see [Assigning users access](/docs/account?topic=account-catalog-access).

  If you don't see what you're expecting in the console based on your permissions, try refreshing your session by going to https://cloud.ibm.com/login.
  {: tip}

## Update an existing version by using the console
{: #update-editor-offering}

When you make specific updates to a software product, such as updating the readme or adding a category, you're required to validate and republish it. Alternatively, you can create a draft of an existing version, update it, and publish the changes immediately. 

1. Go to **Manage** > **Catalogs** > **Private catalogs**, and select **My first catalog** from the list of private catalogs. 
1. Click the apache-two-instances product.
1. Click **Create a draft version to make changes and then publish again** that's displayed in the notification.
1. Click the Edit readme tab.
1. Click the **Edit** icon ![Edit icon](../icons/icon_write.svg), add `This is my updated readme` on a new line, and click **Update** to save your changes.
1. Click the **Actions** icon ![Actions icon](../icons/actions-icon-vertical.svg), and select **Merge changes** to publish the updated version to your account.

### Validate the updated version is available 
{: #create-editor-validate}

1. Click **Catalog** in the console menu bar.
1. Click the Private tab.
1. Select the apache-two-instances product.
1. Click **Readme**.
1. Search for the `This is my updated readme` text.

### Success criteria
{: #update-success-validate}

You can find the new line of text in the readme.

## Update an existing version by using the CLI
{: #update-version-cli}

Before you begin this task, delete the version that you previously created:

1. Go to **Manage** > **Catalogs** > **Private catalogs**, and select **My first catalog** from the list of private catalogs. 
2. Expand the apache-two-instances row, click the **Actions** icon ![Actions icon](../icons/actions-icon-vertical.svg) from the 2.4.41 row, and select **Delete**. The selected version is deleted, and version 2.4.39 remains intact. 
<br> 

Complete the following steps to create a draft version, update it, and merge the changes to the current version of your software.  

  You need the version locator for your software version. To find it, run the `ibmcloud catalog offering list --catalog "My first catalog"` command, and search for version 2.4.39.
  {: important}
    
1. Create a draft version of your software.
    ```
    ibmcloud catalog offering create-draft --version-locator <VERSION_LOCATOR>
    ```
    {: codeblock}
    
1. Set another category.
    ```
    ibmcloud catalog offering add-category --catalog "My first catalog" --offering "apache-two-instances" --category "Integration"
    ```
    {: codeblock}
    
1. Merge the draft update to your software. This action merges the update to the version of your software that's published in your account.   
    ```
    ibmcloud catalog offering merge-draft --version-locator **<VERSION_LOCATOR_OF_DRAFT_VERSION>**
    ```
    {: codeblock}
    
1.  Search for the software in the {{site.data.keyword.cloud_notm}} catalog.
    ```
    ibmcloud catalog get --public | grep apache-two-instances
    ```
    {: codeblock}
    
### Success criteria
{: #existingversion-success-cli}

You successfully completed the task if the updated version is included in the search results. 

## Next steps
{: next-deprestore}

A user with access to a private catalog deprecates and then restores a version of the software. See [Deprecating and restoring a software version](/docs/account?topic=account-dep-restore) for more information.
