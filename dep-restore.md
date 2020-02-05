---

copyright:
  years: 2020
lastupdated: "2020-02-05"

keywords: deprecate offering, restore offering, catalog, catalogs, software

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:external: target="_blank" .external}

# Deprecating and restoring a version of a software offering
{: #dep-restore}

In this tutorial, you deprecate a version of the apache-two-instances offering. Then, you restore the version to the {{site.data.keyword.cloud}} catalog. 
{: shortdesc}

This feature is available only in a closed beta. If you’re interested in participating, contact kala.nenkova@ibm.com.
{: note}

## Before you begin
{: #prereq-restore}

To complete this tutorial, you need to be assigned the editor role on the private catalog service. For more information, see [Assigning users access](/docs/account?topic=account-catalog-access).

  If you don't see what you're expecting in the console based on your permissions, try refreshing your session by going to https://cloud.ibm.com/login.
  {: tip}

## Deprecate a version of a software offering in the console
{: #deprecate-editor}

When you deprecate a version, it is not displayed in the catalog for any user that hasn't installed it. All users who previously installed the offering can still access it. 

1. Go [Manage > Catalogs](https://cloud.ibm.com/content-mgmt/catalogs), and click **My first catalog** from the list of private catalogs.
1. Click the apache-two-instances offering.
1. From the **Version** list, select **2.4.39**. 
1. Click the **Actions** icon ![Actions icon](../icons/actions-icon-vertical.svg), and select **Deprecate**.

### Validate the version is deprecated 
{: #deprecate-validate-editor}

1. Click **Catalog** in the console menu bar.
1. Click the Private tab. 
1. Select apache-two-instances offering. 
1. Verify that only version 2.4.41 is listed in the **Version** list.

### Success criteria
{: #success-deprecate}

Version 2.4.39 of the apache-two-instances offering offering isn't listed in the **Version** list on the Private tab of the catalog.


## Restore the deprecated version in the console
{: #restore-editor}

When you restore a deprecated version, you are required to validate and publish the software offering again.

1. Go to [Manage > Catalogs](https://cloud.ibm.com/content-mgmt/catalogs), and select **My first catalog**.
1. Click the apache-two-instances offering.
1. Click the **Version** list, and select **2.4.39**. 
1. Click the **Actions** icon ![Actions icon](../icons/actions-icon-vertical.svg), and select **Restore**.
1. Confirm that you want to restore the deprecated version.
1. Click the Validate offering tab.
2. Select a cluster from the **Cluster** list, and select **apache-test-deployment** from the **Namespace** list.
3. Click **Validate**.
1. When the offering is validated, click the **Actions** icon ![List of options icon][options-icon], and select **Merge changes**. 

### Validate the version is restored
{: #restore-validate-editor}

1. Click **Catalog** from the console menu bar.
1. Select **My first catalog** from the list of catalogs, and click the Private tab.
1. Select the apache-two-instances offering. 
1. Verify both version 2.4.39 and version 2.4.41 are listed in the **Version** list.

### Success criteria
{: #success-restore-validate}

Both versions of the apache-two-instances offering are included in the **Version** list on the Private tab of the catalog.


## Deprecate a version of a software offering by using the CLI
{: #deprecate-cicd-editor}

You need the version locator for your offering version. To find it, run the `ibmcloud catalog offering list --catalog "My first catalog"` command, and search for version 2.4.39.
{: important}

1. Deprecate a version of your software offering.
    ```
    ibmcloud catalog offering deprecate --version-locator <VERSION_LOCATOR>
    ```
    {: codeblock}
    
1. Search the offerings in the catalog and verify that apache 2.4.39 is deprecated:
    ```
    ibmcloud catalog offering search --catalog "My first catalog"
    ```
    {: codeblock}
    
## Restore a deprecated version by using the CLI
    
When you restore a deprecated version, you are required to validate and publish the software offering again.

1. Restore the offering. This action creates a draft version of the deprecated version.
    ```
    ibmcloud catalog offering deprecate --version-locator <VERSION_LOCATOR>
    ```
    {: codeblock}
        
1. Validate the offering:
    ```
    ibmcloud catalog offering validate --version-locator <LOCATOR> --cluster <CLUSTER> --namespace "apache-test-deployment"
    ```
    {: codeblock}
        
1. Merge the draft version. This action automatically makes version 2.4.39 available in the catalog.  
    
    To find the version-locator for the draft version, run the `ibmcloud catalog offering list --catalog "My first catalog"` command, and search for version 2.4.39-draft.
    {: note}
      
    ```
    ibmcloud catalog offering merge-draft --version-locator **<VERSION_LOCATOR_OF_DRAFT_VERSION>**
    ```
    {: codeblock}
        
1. Search the offerings in the catalog, and verify that apache 2.4.39 is listed.
    ```
    ibmcloud catalog offering get --catalog "My first catalog" --offering "apache"
    ```
    {: codeblock}

### Success criteria
{: #success-cicd-deprecate}

You successfully completed this task if you ran all CLI commands with the expected results.

## Next steps
{: #next-feedback}

We'd love to know what you think about the catalog management beta! We put together the following surveys to help with submitting your feedback:

* [Survey: Filtering the {{site.data.keyword.cloud_notm}} catalog for all account users](https://airtable.com/shrOeKPjUz5bzw02c){: external}
* [Survey: Filtering the {{site.data.keyword.cloud_notm}} catalog at a private catalog level](https://airtable.com/shrSb9if7nPO36jhh){: external}
* [Survey: Adding your own software to a private catalog](https://airtable.com/shr6Fornt8WwtAKPZ){: external}

