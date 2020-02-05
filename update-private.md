---

copyright:
  years: 2020
lastupdated: "2020-02-05"

keywords: catalog, private catalog, update, private catalog offering, update version

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:new_window: target="_blank"}

# Updating a software offering
{: #update-private}

In this tutorial, you update the apache-two-instances offering by updating the readme of the existing version and adding a new version. 
{: shortdesc}

This feature is available only in a closed beta program. If you’re interested in participating, contact kala.nenkova@ibm.com.
{: note}

## Before you begin
{: #prereq-update}

To complete this tutorial, you need to be assigned the editor role on the private catalog service. With this type of access, you can create private catalogs and set filters that apply only to users with access to your private catalog. You can also view the account-level filters on the Settings page, but you can't update them. For more information, see [Assigning users access](/docs/account?topic=account-catalog-access).

  If you don't see what you're expecting in the console based on your permissions, try refreshing your session by going to https://cloud.ibm.com/login.
  {: tip}

## Update an existing version in the console
{: #update-editor-offering}

When you make specific updates to a software offering, such as updating the readme or adding a category, you're required to validate and republish the offering. Alternatively, you can create a draft of an existing version, update it, and publish the changes immediately. 

1. Go to [Manage > Catalogs](https://cloud.ibm.com/content-mgmt/catalogs), and click **My first catalog** from the list of private catalogs. 
1. Click the apache-two-instances offering.
1. Click **Create a draft version to make changes and then publish again**.
1. Click the Edit readme tab.
1. Click the **Edit** icon ![Edit icon](../icons/icon_write.svg), add `This is my updated readme` on a new line, and click **Update** to save your changes.
1. Click the **Actions** icon ![Actions icon](../icons/actions-icon-vertical.svg), and select **Merge changes** to publish the updated version to your account.

### Validate the updated version is available 
{: #create-editor-validate}

1. Click **Catalog** in the console menu bar.
1. Click the Private tab.
1. Select the apache-two-instances offering.
1. Click **Readme**.
1. Search for `This is my updated readme`.

### Success criteria
{: #update-success-validate}

You can find the new line of text in the readme.

## Add a new version in the console
{: #update-editor-import}

Complete the following steps to add a new version of the apache-two-instances offering.  

1. Go to [Manage > Catalogs](https://cloud.ibm.com/content-mgmt/catalogs), and click **My first catalog** from the list of private catalogs.
2. Click the apache-two-instances offering.
1. Click **Add new version**, enter `https://charts.bitnami.com/ibm/apache-7.3.2.tgz` as the TGZ URL, and click **Add**. This action adds version 2.4.41 from apache chart version 7.3.2.
1. Click the Validate offering tab.
2. Select a Kubernetes cluster, and enter a namespace value.
1. Click the **Actions** icon ![Actions icon](../icons/actions-icon-vertical.svg), and select **Publish to account**.

### Validate the new version is available 
{: #update-validate-version}

1. Click **Catalog** in the console menu bar.
1. Click the Private tab.
1. Select the apache-two-instances offering.
1. Verify that both version 2.4.41 and version 2.4.39 are listed in the **Version** list.

### Success criteria
{: #update-validate-version}

The new version number is included in the **Version** list on the Private tab of the catalog.

## Update an existing version by using the CLI
{: #update-version-cli}

Before you begin this task, delete the version that you previously created:

1. Go to [Manage > Catalogs](https://cloud.ibm.com/content-mgmt/catalogs), and click **My first catalog** from the list of private catalogs.
2. Expand the apache-two-instances row, click the **Actions** icon ![Actions icon](../icons/actions-icon-vertical.svg) from the 2.4.41 row, and select **Delete**. The selected version is deleted, and version 2.4.39 remains intact. 
<br>

Complete the following steps to create a draft version, update it, and merge the changes to the current version of your software offering.  

  You need the version locator for your offering version. To find it, run the `ibmcloud catalog offering list --catalog "My first catalog"` command, and search for version 2.4.39.
  {: important}
    
1. Create a draft version of your software offering.
    ```
    ibmcloud catalog offering create-draft --version-locator <VERSION_LOCATOR>
    ```
    {: codeblock}
    
1. Set another category.
    ```
    ibmcloud catalog offering add-category --catalog "My first catalog" --offering "apache-two-instances" --category "Integration"
    ```
    {: codeblock}
    
1. Merge the draft update to your software offering. This action merges the update to the version of your software offering that's published in your account.   
    ```
    ibmcloud catalog offering merge-draft --version-locator **<VERSION_LOCATOR_OF_DRAFT_VERSION>**
    ```
    {: codeblock}
    
1.  Search for the offering in the {{site.data.keyword.cloud_notm}} catalog.
    ```
    ibmcloud catalog get --public | grep apache-two-instances
    ```
    {: codeblock}
    
### Success criteria
{: #existingversion-success-cli}

You successfully completed the task if the updated version is included in the search results. 

## Add a new version by using CLI
{: #update-cicd-import}

Complete the following steps to add a new version, validate it, and publish it to your account:

1. Add a new version of the offering to your private catalog.  
    ```
    ibmcloud catalog offering import-version --catalog "My first catalog" --offering "apache-two-instances" --zipurl https://charts.bitnami.com/ibm/apache-7.3.2.tgz
    ```
    {: codeblock}
    
1. Validate the offering.
    ```
    ibmcloud catalog offering validate --version-locator <LOCATOR> --cluster <CLUSTER> --namespace "apache-test-deployment"
    ```
    {: codeblock}
    
    This operation runs a few minutes. You can check the validation status by querying the offering and checking the current state of the draft version. 
    
    ```
    ibmcloud catalog offering get --catalog "My first catalog" --offering "apache-two-instances"
    ```
    {: codeblock}
    
1. Publish the new version to your account. This step adds another version in the existing tile on the Private tab in the {{site.data.keyword.cloud_notm}} catalog.
    ```
    ibmcloud catalog offering publish-to-account --version-locator <LOCATOR>
    ```
    {: codeblock}
    
1.  Search for the offering in the {{site.data.keyword.cloud_notm}} catalog.
    ```
    ibmcloud catalog get --public | grep apache-two-instances
    ```
    {: codeblock}

### Success criteria
{: #newversion-success-cli}

You successfully completed the task if the new version is included in the search results. 

## Next steps
{: next-deprestore}

A user with access to a private catalog deprecates and then restores a version of the apache-two-instances offering. See [Deprecating and restoring a version of a software offering](/docs/account?topic=account-dep-restore) for more information.
