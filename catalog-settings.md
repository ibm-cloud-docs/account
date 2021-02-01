---

copyright:
  years: 2019, 2021
lastupdated: "2021-02-01"

keywords: catalog, private catalogs, visibility, filter catalog, hide product, catalog filtering, enterprise, account group, child account, account, restrict

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:external: target="_blank" .external}

# Managing catalog settings
{: #filter-account}

As the account owner or administrator, you can manage the settings for all catalogs across your account. Management tasks include setting the visibility of the {{site.data.keyword.cloud}} catalog and controlling access to products in the public catalog and private catalogs for users in your account.
{: shortdesc}

You need the [administrator role on the catalog management service](/docs/account?topic=account-account-services#catalog-management-account-management) to perform these tasks.

## Updating the visibility of the {{site.data.keyword.cloud_notm}} catalog
{: #set-public-visibility}

Users in your account have access to all products in the public catalog by default. To update what products are visible to users, go to **Manage** > **Catalogs** > **Settings** in the {{site.data.keyword.cloud_notm}} console. 

If you don't have any private catalogs in your account and you turn off the visibility of the public catalog, users can't create instances of any products. Be sure to [create a private catalog](/docs/account?topic=account-restrict-by-user) before you update this setting. 
{: note}

## Managing access to products for all users
{: #set-account-filters}

You can use filters to manage which products in the public catalog are available to all users in your account. For example, you might want to restrict access to third-party products. Or, you might want users to work with a specific software type. 

If your account is a parent account in an {{site.data.keyword.cloud_notm}} enterprise, the filters that you set apply to all child account groups and accounts. For more information, see [Managing products for an an {{site.data.keyword.cloud_notm}} enterprise](/docs/account?topic=account-catalog-enterprise-restrict).
{: tip}

1. In the console, go to **Manage** > **Catalogs** > **Settings**. 
2. Confirm that the visibility of the public catalog is set to **On**.
3. In the What products are available? section, select **Exclude all products in the {{site.data.keyword.cloud_notm}} catalog**.
4. Set one or more [filters](#catalog-filters-customize) to customize what products are available by category.
5. (Optional) Add exceptions to the filter rules that you set in the previous step. 
6. Use the **Preview** table to confirm your selections, and click **Update**.

## Managing access to products for specific users 
{: #set-private-filters}

Set filters at a private catalog level for fine-grained control of which products in the public catalog are available only to the users you choose.   

1. In the console, go to **Manage** > **Catalogs**, **Private catalogs**. 
2. Select a catalog from the list to navigate to its details page. 

  The **Products in the {{site.data.keyword.cloud_notm}} catalog** table that's displayed on the page shows the list of products that are available at the account level. The availability is based on the filters the account owner or administator set. Account-level filters apply to all the private catalogs in the account. 
  {: tip}
  
3. Click **Manage filters**.
3. Select to include or exclude all products in the public catalog. 
4. Set one or more [filters](#catalog-filters-customize) to customize what products are available by category. 
5. (Optional) Add exceptions to the filter rules that you set in the previous step. 
6. Click **Update**. 
7. Go to the Settings page and turn off the visibility of the public catalog.  
7. To give users access to work with the products in the private catalog, assign them the [viewer role on the catalog management service](/docs/account?topic=account-account-services#catalog-management-account-management).  
<br>
<br>
For more detailed examples of how you can leverage filtering at the private catalog level, see [Customizing your private catalogs](/docs/account?topic=account-restrict-by-user).

## Catalog filters
{: #catalog-filters-customize}

The following table lists the filters that you can use to customize which products in the public catalog are available to users in your account. 

| Option | Description |
|------------------|-------|
| AI / Machine Learning | Products that enable systems to learn from data rather than through explicit programming. |
| Analytics | Products that facilitate the analysis of data, typically large sets of business data, by the use of mathematics, statistics, and other means. |
| Blockchain | Products that facilitate the process of recording transactions and tracking assets in a business network. |
| Compute | Infrastructure resources that serve as the basis for building apps in the cloud. |
| Containers | A standard unit of software that packages up code and all its dependencies so the app runs quickly and reliably from one computing environment to another. |
| Databases | Products that provide some form of access to a database without the need for setting up physical hardware, installing software, or configuring for performance. |
| Developer Tools | Products that support developing, testing, and debugging software. |
| Integration | Products that facilitate the connection of data, apps, APIs, and devices across an organization to be more efficient, productive, and agile. |
| Internet of Things | Products that support receiving and transferring data over wireless networks without human intervention. |
| Logging and Monitoring | Products that support receiving and transferring data over wireless networks without human intervention. |
| Mobile | Products with specific or special utility for users creatings things to be used on mobile devices. |
| Networking | Products that support or augment the linking of computers so they can operate interactively. |
| Security | Products that provide the protection of stored data from theft, leakage, and deletion. |
| Storage  | Products that support data to be created, read, updated, and deleted. |
{: caption="Table 1. Options for filtering by category" caption-side="top"}
{: #category-custom}
{: tab-title="Category"}
{: tab-group="customcatalogfilters"}
{: class="simple-tab-table"}
{: summary="Use the buttons before the table to change the context of the table. The column headers identify the options for fitering based on filter type."}

| Option | Description |
|--------------|-------|
| EU Supported | Support for the service is provided by {{site.data.keyword.cloud_notm}} support team members that are located in the European Union (EU) region. |
| HIPAA Enabled | The service is designated as HIPAA ready, meaning processing, storing, and handling Protected Health Information (PHI) in the service is supported. |
| IAM-enabled | The service is enabled to use {{site.data.keyword.cloud_notm}} Identity and Access Management (IAM) for access control. Access policies are used to assign users and service IDs access to specific resources in an account.|
| Service Endpoint Supported | The service can be connected to over the {{site.data.keyword.cloud_notm}} private network instead of the public network. Connecting directly to service endpoints doesn't require internet access, providing increased security. |
{: caption="Table 2. Options for filtering by compliance" caption-side="top"}
{: #compliance-custom}
{: tab-title="Compliance"}
{: tab-group="customcatalogfilters"}
{: class="simple-tab-table"}
{: summary="Use the buttons before the table to change the context of the table. The column headers identify the options for fitering based on filter type."}

| Option | Description |
|--------------|-------|
| Community | The product is provided by open source communities outside of {{site.data.keyword.IBM_notm}}. If the root cause analysis determines that the issue is a defect in the product, {{site.data.keyword.IBM_notm}} isn't required to provide a fix. |
| {{site.data.keyword.IBM_notm}} | The lifecycle and operations of the product are the responsibility of {{site.data.keyword.IBM_notm}}. |
| Third party | Support for the product is the responsibility of the third-party provider. If the root cause analysis determines that the issue is a defect in the product, {{site.data.keyword.IBM_notm}} isn't required to provide a fix. However, {{site.data.keyword.IBM_notm}} shares analysis with the third-party provider, if needed, and can work with the third-party provider to help solve the issue. |
{: caption="Table 3. Options for filtering by provider" caption-side="top"}
{: #provider-custom}
{: tab-title="Provider"}
{: tab-group="customcatalogfilters"}
{: class="simple-tab-table"}
{: summary="Use the buttons before the table to change the context of the table. The column headers identify the options for fitering based on filter type."} 

| Option | Description |
|--------------|-------|
| Beta | The product is available for evaluation and testing purposes. Beta products are not intended for production use. |
| Experimental | The product is available for evaluation and testing purposes, and might be unstable or not compatible with previous versions. The product can be discontinued with short notice.
| Deprecated | The product is supported but no longer recommended and that might become obsolete. |
{: caption="Table 4. Options for filtering by release" caption-side="top"}
{: #release-custom}
{: tab-title="Release"}
{: tab-group="customcatalogfilters"}
{: class="simple-tab-table"}
{: summary="Use the buttons before the table to change the context of the table. The column headers identify the options for fitering based on filter type."}

| Option | Description |
|--------------|-------|
| Location | The general area for networking options. Each location has a region, one or more zones, and one or more data centers. For example, `Dallas` and `Osaka`. For more information, see [Locations for resource deployment](https://cloud.ibm.com/docs/overview?topic=overview-locations). |
| Region | A defined geographic territory in which apps, services, and resources are deployed. For example, `us-south` and `jp-osa`. For more information, see [multizone regions](/docs/overview?topic=overview-locations#mzr-table) and [single-zone regions](/docs/overview?topic=overview-locations#szr-table). |
| Zone | An isolated location within regions. For example, `us-south-2` and `jp-osa-3`. Each region can have one or more zones. |
| Data center | The physical location of the servers that provide cloud services. For example, `DAL12` and `OSA23`. For more information, see [Data centers](/docs/overview?topic=overview-locations#data-centers). |
{: caption="Table 5. Options for filtering by location" caption-side="top"}
{: #location-custom}
{: tab-title="Location"}
{: tab-group="customcatalogfilters"}
{: class="simple-tab-table"}
{: summary="Use the buttons before the table to change the context of the table. The column headers identify the options for fitering based on filter type."}




 



