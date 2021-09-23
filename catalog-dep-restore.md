---

copyright:
  years: 2020, 2021
lastupdated: "2021-09-22"

keywords: deprecate software, restore software, catalog, catalogs, software, private catalog

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:go: .ph data-hd-programlang='go'}
{:javascript: .ph data-hd-programlang='javascript'}
{:java: .ph data-hd-programlang='java'}
{:python: .ph data-hd-programlang='python'}
{:important: .important}
{:external: target="_blank" .external}
{:ui: .ph data-hd-interface='ui'}
{:cli: .ph data-hd-interface='cli'}
{:api: .ph data-hd-interface='api'}

# Deprecating and restoring software versions
{: #dep-restore}

In this tutorial, you deprecate a version of the apache-two-instances software instance. Then, you restore the version to the {{site.data.keyword.cloud}} catalog.
{: shortdesc}

## Before you begin
{: #prereq-restore}

To complete this tutorial, you need to be assigned the editor role on the catalog management service. For more information, see [Assigning users access](/docs/account?topic=account-catalog-access).

   If you don't see what you're expecting in the console based on your permissions, try refreshing your session by going to https://cloud.ibm.com/login.
   {: tip}

## Deprecate a software version in the console
{: #deprecate-editor}
{: ui}

When you deprecate a version, it is not displayed in the catalog for any user that hasn't installed it. All users who previously installed the software can still access it. 

1. Go **Manage** > **Catalogs** > **Private catalogs**, and select **My first catalog** from the list of private catalogs.
1. Click **apache-two-instances**.
1. From the **Version** list, select **2.4.39**. 
1. Click the **Actions** icon ![Actions icon](../icons/actions-icon-vertical.svg "Actions"), and select **Deprecate**.

### Validate the version is deprecated 
{: #deprecate-validate-editor}

1. Click **Catalog** in the console menu bar.
1. Select **My first catalog** from the list of catalogs.
1. Click the Private tab > **apache-two-instances**. 
1. Verify that only version 2.4.41 is listed in the **Version** list.

## Restore the deprecated version in the console
{: #restore-editor}
{: ui}

When you restore a deprecated version, you are required to validate and publish the software again.

1. Go to **Manage** > **Catalogs** > **Private catalogs**, and select **My first catalog**.
1. Click **apache-two-instances**.
1. Click the **Version** list, and select **2.4.39**. 
1. Click the **Actions** icon ![Actions icon](../icons/actions-icon-vertical.svg "Actions"), and select **Restore**.
1. Confirm that you want to restore the deprecated version.
1. Click the Validate offering tab.
2. Select a cluster from the **Cluster** list, and select **apache-test-deployment** from the **Namespace** list.
3. Click **Validate**.
1. When the software is validated, click the **Actions** icon ![Actions icon](../icons/actions-icon-vertical.svg "Actions"), and select **Merge changes**. 

### Validate the version is restored
{: #restore-validate-editor}

1. Click **Catalog** from the console menu bar.
1. Select **My first catalog** from the list of catalogs.
1. Click the Private tab > **apache-two-instances**. 
1. Verify that both version 2.4.39 and version 2.4.41 are listed in the **Version** list.


## Deprecate a software version by using the CLI
{: #deprecate-cicd-editor}
{: cli}

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
{: #restore-cicd-editor}
{: cli}
    
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

## Deprecate an existing version by using the API
{: #deprecate-version-api}
{: api}

You can programmatically deprecate a version by calling the Catalog Management API as shown in the following sample request. For detailed information about the API, see [Catalog Management API](https://test.cloud.ibm.com/apidocs/resource-catalog/private-catalog?code=python#deprecate-version){: external}.


```java
String versionLocator = "{versionLocator}";
DeprecateVersionOptions depOptions = new DeprecateVersionOptions.Builder().versionLocId(versionLocator).build();
Response<Void> response = service.deprecateVersion(depOptions).execute();
System.out.println(response.getResult());
```
{: codeblock}
{: java}

```javascript
versionLocator = "{versionLocator}";
response = await service.deprecateVersion({ 'versionLocId': versionLocator});
console.log(response);
}).catch(err => {});
```
{: codeblock}
{: javascript}

```python
versionLocator = "{versionLocator}"
response = self.service.deprecate_version(version_loc_id=versionLocator)
print(response)
```
{: codeblock}
{: python}

```go
versionLocator := "{versionLocator}"
depOptions := service.NewDeprecateVersionOptions(versionLocator)
response, _ := service.DeprecateVersion(depOptions)
fmt.Println(response)
```
{: codeblock}
{: go}

## Restore a deprecated version by using the API
{: #restore-version-api}
{: api}
This action can be done only through the UI or CLI. To see the steps, switch to the UI or CLI instructions.
