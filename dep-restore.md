---

copyright:
  years: 2020
lastupdated: "2020-04-02"

keywords: deprecate software, restore software, catalog, catalogs, software 

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:external: target="_blank" .external}

# Deprecating and restoring software versions
{: #dep-restore}

In this tutorial, you deprecate a version of the apache-two-instances software instance. Then, you restore the version to the {{site.data.keyword.cloud}} catalog. 
{: shortdesc}

## Before you begin
{: #prereq-restore}

To complete this tutorial, you need to be assigned the editor role on the catalog management service. For more information, see [Assigning users access](/docs/account?topic=account-catalog-access).

  If you don't see what you're expecting in the console based on your permissions, try refreshing your session by going to https://cloud.ibm.com/login.
  {: tip}

## Deprecate a software version by using console
{: #deprecate-editor}

When you deprecate a version, it is not displayed in the catalog for any user that hasn't installed it. All users who previously installed the software can still access it. 

1. Go **Manage** > **Catalogs** > **Private catalogs**, and select **My first catalog** from the list of private catalogs.
1. Click **apache-two-instances**.
1. From the **Version** list, select **2.4.39**. 
1. Click the **Actions** icon ![Actions icon](../icons/actions-icon-vertical.svg), and select **Deprecate**.

### Validate the version is deprecated 
{: #deprecate-validate-editor}

1. Click **Catalog** in the console menu bar.
1. Select **My first catalog** from the list of catalogs.
1. Click the Private tab > **apache-two-instances**. 
1. Verify that only version 2.4.41 is listed in the **Version** list.


## Restore the deprecated version by using the console
{: #restore-editor}

When you restore a deprecated version, you are required to validate and publish the software again.

1. Go to **Manage** > **Catalogs** > **Private catalogs**, and select **My first catalog**.
1. Click **apache-two-instances**.
1. Click the **Version** list, and select **2.4.39**. 
1. Click the **Actions** icon ![Actions icon](../icons/actions-icon-vertical.svg), and select **Restore**.
1. Click the Validate offering tab.
2. Select a cluster from the **Cluster** list, and select **apache-test-deployment** from the **Namespace** list.
3. Click **Validate**.
1. When the software is validated, click the **Actions** icon ![Actions icon](../icons/actions-icon-vertical.svg), and select **Merge changes**. 

### Validate the version is restored
{: #restore-validate-editor}

1. Click **Catalog** from the console menu bar.
1. Select **My first catalog** from the list of catalogs.
1. Click the Private tab > **apache-two-instances**. 
1. Verify that both version 2.4.39 and version 2.4.41 are listed in the **Version** list.


## Deprecate a software version by using the CLI
{: #deprecate-cicd-editor}

You need the version locator for your software version. To find it, run the **`ibmcloud catalog offering list --catalog "My first catalog"`** command, and search for version 2.4.39.
{: important}

1. Deprecate the existing software version.
    ```
    ibmcloud catalog offering deprecate --version-locator <VERSION_LOCATOR>
    ```
    {: codeblock}
    
1. Search the catalog and verify that apache 2.4.39 is deprecated:
    ```
    ibmcloud catalog offering search --catalog "My first catalog"
    ```
    {: codeblock}
    
## Restore a deprecated version by using the CLI
    
When you restore a deprecated version, you are required to validate and publish the software again.

1. Restore the deprecated version. This action creates a draft version.
    ```
    ibmcloud catalog offering restore --version-locator <VERSION_LOCATOR>
    ```
    {: codeblock}
        
1. Validate the software:
    ```
    ibmcloud catalog offering validate --version-locator **<VERSION_LOCATOR_OF_DRAFT_VERSION>** --cluster <CLUSTER> --namespace "apache-test-deployment"
    ```
    {: codeblock}
        
1. Merge the draft version. This action automatically makes version 2.4.39 available in the catalog.  
      
    ```
    ibmcloud catalog offering merge-draft --version-locator **<VERSION_LOCATOR_OF_DRAFT_VERSION>**
    ```
    {: codeblock}
        
1. Search the catalog and verify that apache 2.4.39 is listed.
    ```
    ibmcloud catalog offering get --catalog "My first catalog" --offering "apache"
    ```
    {: codeblock}

