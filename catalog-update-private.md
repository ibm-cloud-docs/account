---

copyright:
  years: 2020
lastupdated: "2020-08-13"

keywords: catalog, private catalog, update, private catalog product, update version, versions

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}

# Updating a version of your software
{: #update-private}

To update the software that's in your private catalog, you can add a new version or update and republish an existing version. 
{: shortdesc}

## Before you begin
{: #prereq-update}

To complete this task, you need to be assigned the editor role on the catalog management service. With this type of access, you can create private catalogs and set filters that apply only to users with access to your private catalog. You can also view the account-level filters on the Settings page, but you can't update them. For more information, see [Assigning users access](/docs/account?topic=account-catalog-access).

## Update an existing version by using the console
{: #update-editor-offering}

When you make specific updates to a software product, such as updating the readme or adding a category, you're required to validate and republish it. Alternatively, you can create a draft of an existing version, update it, and publish the changes immediately. 

1. Go to **Manage** > **Catalogs** > **Private catalogs**, and select your catalog from the list. 
1. Click the name of your software product.
1. Click **Create a draft version to make changes and then publish again** in the notification that's displayed on the page. 
1. Click the Edit readme tab.
1. Click the **Edit** icon ![Edit icon](../icons/icon_write.svg) > **Update** to save your changes.
1. Click the **Actions** icon ![Actions icon](../icons/actions-icon-vertical.svg), and select **Merge changes** to publish the updated version to your account.

## Update an existing version by using the CLI
{: #update-version-cli}

Complete the following steps to create a draft version, update it, and merge the changes to the current version of your software.  

  You need the version locator for your software. To find it, run the **`ibmcloud catalog offering list --catalog "your-private-catalog"`** command and search for the existing version number.
  {: important}
    
1. Create a draft version of your software.
    ```
    ibmcloud catalog offering create-draft --version-locator <VERSION_LOCATOR>
    ```
    {: codeblock}
    
1. Set another category.
    ```
    ibmcloud catalog offering add-category --catalog "your-private-catalog" --offering "your-software" --category "category-type"
    ```
    {: codeblock}
    
1. Merge the draft update to your software. This action merges the update to the version of your software that's published in your account.   
    ```
    ibmcloud catalog offering merge-draft --version-locator **<VERSION_LOCATOR_OF_DRAFT_VERSION>**
    ```
    {: codeblock}
    
1.  Search for the software in the {{site.data.keyword.cloud_notm}} catalog.
    ```
    ibmcloud catalog get --public | grep your-software
    ```
    {: codeblock}
