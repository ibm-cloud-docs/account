---

copyright:
  years: 2019, 2023

lastupdated: "2023-03-13"


keywords: catalog, private catalogs, visibility, filter catalog, hide product, catalog filtering, enterprise, account group, child account, account, restrict

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Managing catalog settings
{: #filter-account}

As the account owner or administrator, you can manage the settings for all catalogs across your account. Management tasks include setting the visibility of the {{site.data.keyword.cloud}} catalog and controlling access to products in the public catalog and private catalogs for users in your account.
{: shortdesc}

## Before you begin
{: #set-before-begin}

1. Verify that you're using a Pay-As-You-Go or Subscription account. See [Viewing your account type](/docs/account?topic=account-account_settings#view-acct-type) for more details.

1. Verify that you have the [administrator role on the catalog management service](/docs/account?topic=account-account-services#catalog-management-account-management).

1. If you want users to have access to products in your account, make sure that you [create a private catalog](/docs/account?topic=account-restrict-by-user&interface=ui) before you update the {{site.data.keyword.cloud_notm}} catalog visibility setting.

## Updating the visibility of the {{site.data.keyword.cloud_notm}} catalog in the console
{: #set-public-visibility}
{: ui}

Users in your account have access to all products in the public catalog by default. If you turn off the visibility of the public {{site.data.keyword.cloud_notm}} catalog, users can't use the console to create instances of products unless you give them access to a private catalog in your account.

To update what products are visible to users, go to **Manage** > **Catalogs** > **Settings** in the {{site.data.keyword.cloud_notm}} console.

Some products aren't affected by catalog visibility settings. Users can create instances of these products by using an API or the CLI. For more information, see [Known issues and limitations](/docs/account?topic=account-known-issues).
{: important}

## Managing access to products for all users in the console
{: #set-account-filters}
{: ui}

You can use filters to manage which products in the public catalog are available to all users in your account. For example, you might want to restrict access to third-party products. Or, you might want users to work with a specific software type. If your account is a parent account in an {{site.data.keyword.cloud_notm}} enterprise, the filters that you set apply to all child account groups and accounts. For more information, see [Managing products for {{site.data.keyword.cloud_notm}} enterprise](/docs/account?topic=account-catalog-enterprise-restrict).


1. Go to **Manage** > **Catalogs** > **Settings** in the {{site.data.keyword.cloud_notm}} console.
2. Confirm that the visibility of the public catalog is set to **On**.
3. In the What products are available? section, select **Exclude all products in the {{site.data.keyword.cloud_notm}} catalog**.
4. Set one or more [filters](#catalog-filters-customize) to customize what products are available by category.
5. (Optional) Add exceptions to the filter rules that you set in the previous step.
6. Use the **Preview** table to confirm your selections, and click **Update**.

## Managing access to products for specific users in the console
{: #set-private-filters}
{: ui}

Set filters at a private catalog level for fine-grained control of which products in the public catalog are available only to the users you choose.

1. Go to **Manage** > **Catalogs**, **Private catalogs** in the {{site.data.keyword.cloud_notm}} console.
2. Select a catalog from the list to navigate to its details page.

   The **Products in the {{site.data.keyword.cloud_notm}} catalog** table that's displayed on the page shows the list of products that are available at the account level. The availability is based on the filters the account owner or administrator set. Account-level filters apply to all the private catalogs in the account.
   {: tip}

3. Click **Manage filters**.
4. Select to include or exclude all products in the public catalog.
5. Set one or more [filters](#catalog-filters-customize) to customize what products are available by category.
6. (Optional) Add exceptions to the filter rules that you set in the previous step.
7. Click **Update**.
8. Go to the Settings page and turn off the visibility of the public catalog.
9. To give users access to work with the products in the private catalog, assign them the [viewer role on the catalog management service](/docs/account?topic=account-account-services#catalog-management-account-management).

For more detailed examples of how you can leverage filtering at the private catalog level, see [Customizing your private catalogs](/docs/account?topic=account-restrict-by-user).

## Updating the visibility of the {{site.data.keyword.cloud_notm}} catalog by using the CLI
{: #set-public-visibility-cli}
{: cli}

Users in your account have access to all products in the {{site.data.keyword.cloud_notm}} public catalog by default. You can make products available only to the users you choose by turning off visibility to the {{site.data.keyword.cloud_notm}} catalog and adding the products to your private catalogs. Use the following command to turn off visibility of the public catalog to all users in your account.

```bash
ibmcloud catalog filter hide-ibm-public-catalog
```
{: codeblock}

## Managing access to products for all users by using the CLI
{: #set-account-filters-cli}
{: cli}

You can use filters to manage which products in the public catalog are available to all users in your account. For example, you might want to restrict access to third-party products. Or, you might want users to work with a specific software type.

If your account is a parent account in an {{site.data.keyword.cloud_notm}} enterprise, the filters that you set apply to all child account groups and accounts. For more information, see [Managing products for {{site.data.keyword.cloud_notm}} enterprise](/docs/account?topic=account-catalog-enterprise-restrict).
{: tip}

1. Create a new filter.
   ```bash
   ibmcloud catalog filter create [--catalog CATALOG] [--category CATEGORY] [--compliance COMPLIANCE] [--deployment-target TARGET] [--exclude-list LIST] [--include-all ALL] [--include-list LIST] [--offering-format FORMAT] [--pricing-plan PLAN] [--provider PROVIDER] [--release RELEASE] [--type TYPE]
   ```
   {: codeblock}

   When the `--catalog CATALOG` command is not specified, the filter is created at the account level.
1. Target an account group by specifying the command option `--account-group ACCOUNT GROUP`.
1. Update the filter to include or exclude a particular product or products. See the [Catalog management CLI](/docs/cli?topic=cli-manage-catalogs-plugin#create-filter) guidance for command options or run the `ibmcloud catalog filter options` command to retrieve the filter options for each filter category.

## Managing access to products for specific users by using the CLI
{: #set-private-filters-cli}
{: cli}

Set filters at a private catalog level for fine-grained control of which products in the public catalog are available only to the users you choose.

1. Create a new filter.
   ```bash
   ibmcloud catalog filter create [--catalog CATALOG] [--category CATEGORY] [--compliance COMPLIANCE] [--deployment-target TARGET] [--exclude-list LIST] [--include-all ALL] [--include-list LIST] [--offering-format FORMAT] [--pricing-plan PLAN] [--provider PROVIDER] [--release RELEASE] [--type TYPE]
   ```
   {: codeblock}

   Make sure to specify the `--catalog CATALOG` command option. When `--catalog CATALOG` is not specified, the filter is created at the account level.
1. Target an account group by specifying the command option `--account-group ACCOUNT GROUP`.
1. Update the filter to include or exclude a particular product or products. See the [Catalog management CLI](/docs/cli?topic=cli-manage-catalogs-plugin#create-filter) guidance for command options or run the `ibmcloud catalog filter options` command to retrieve the filter options for each filter category.

## Updating the visibility of the {{site.data.keyword.cloud_notm}} catalog by using the API
{: #set-public-visibility-api}
{: api}

Users in your account have access to all products in the {{site.data.keyword.cloud_notm}} public catalog by default. You can make products available only to the users you choose by turning off visibility to the {{site.data.keyword.cloud_notm}} catalog and adding the products to your private catalogs. Use the following command to turn off visibility of the public catalog to all users in your account.

```bash
curl -X "PUT" "https://cm.globalcatalog.cloud.ibm.com/api/v1-beta/catalogaccount"
-H "accept: */*"
-H "Authorization: {iam-bearer-token}"
-d '{"id":"string","hide_IBM_cloud_catalog":true,"account_filters":{"include_all":true,"category_filters":{"additionalProp1":{"include":true,"filter":{"filter_terms":["string"]}},"additionalProp2":{"include":true,"filter":{"filter_terms":["string"]}},"additionalProp3":{"include":true,"filter":{"filter_terms":["string"]}}},"id_filters":{"include":{"filter_terms":["string"]},"exclude":{"filter_terms":["string"]}}}}'
```
{: codeblock}

<!---
```java
String id = "{id}";
Filters accountFilters = {accountFilters};
UpdateCatalogAccountOptions updateOptions = new UpdateCatalogAccountOptions.Builder().id(id).accountFilters(accountFilters).build();
Response<Void> response = service.updateCatalogAccount(updateOptions).execute();
System.out.println(response.getResult());
```
{: codeblock}
{: java}

```javascript
id = "{id}";
accountFilters = {accountFilters};
response = await service.updateCatalogAccount({ 'id': id, 'accountFilters': accountFilters });
console.log(response);
```
{: codeblock}
{: javascript}

```python
id="{id}"
accountFilters={accountFilters}
response = self.service.update_catalog_account(id=id, account_filters=accountFilters)
print(response)
```
{: codeblock}
{: python}

```go
id := "{id}"
accountFilters := {accountFilters}
updateOptions := service.NewUpdateCatalogAccountOptions()
updateOptions.SetID(id)
updateOptions.AccountFilters(accountFilters)
response, _ := service.UpdateCatalogAccount(updateOptions)
fmt.Println(response)
```
{: codeblock}
{: go}
-->

Make sure the `hide_IBM_cloud_catalog` field has a Boolean value of `true` to hide the public catalog in this account. Alternatively, you can give the `include_all` field a Boolean value of `false` for each `account_filters` object to exclude all of the public catalog.

See the [Catalog Management API](/apidocs/resource-catalog/private-catalog?code=curl#update-catalog-account){: external} for more information.

## Managing access to products for all users by using the API
{: #set-account-filters-api}
{: api}

You can use filters to manage which products in the public catalog are available to all users in your account. For example, you might want to restrict access to third-party products. Or, you might want users to work with a specific software type.

If your account is a parent account in an {{site.data.keyword.cloud_notm}} enterprise, the filters that you set apply to all child account groups and accounts. For more information, see [Managing products for {{site.data.keyword.cloud_notm}} enterprise](/docs/account?topic=account-catalog-enterprise-restrict).
{: tip}

```bash
curl -X "PUT" "https://cm.globalcatalog.cloud.ibm.com/api/v1-beta/catalogaccount"
-H "accept: */*"
-H "Authorization: {iam-bearer-token}"
-d '{"id":"string","hide_IBM_cloud_catalog":true,"account_filters":{"include_all":true,"category_filters":{"additionalProp1":{"include":true,"filter":{"filter_terms":["string"]}},"additionalProp2":{"include":true,"filter":{"filter_terms":["string"]}},"additionalProp3":{"include":true,"filter":{"filter_terms":["string"]}}},"id_filters":{"include":{"filter_terms":["string"]},"exclude":{"filter_terms":["string"]}}}}'
```
{: codeblock}

<!---
```java
String id = "{id}";
Filters accountFilters = {accountFilters};
UpdateCatalogAccountOptions updateOptions = new UpdateCatalogAccountOptions.Builder().id(id).accountFilters(accountFilters).build();
Response<Void> response = service.updateCatalogAccount(updateOptions).execute();
System.out.println(response.getResult());
```
{: codeblock}
{: java}

```javascript
id = "{id}";
accountFilters = {accountFilters};
response = await service.updateCatalogAccount({ 'id': id, 'accountFilters': accountFilters });
console.log(response);
```
{: codeblock}
{: javascript}

```python
id="{id}"
accountFilters={accountFilters}
response = self.service.update_catalog_account(id=id, account_filters=accountFilters)
print(response)
```
{: codeblock}
{: python}

```go
id := "{id}"
accountFilters := {accountFilters}
updateOptions := service.NewUpdateCatalogAccountOptions()
updateOptions.SetID(id)
updateOptions.AccountFilters(accountFilters)
response, _ := service.UpdateCatalogAccount(updateOptions)
fmt.Println(response)
```
{: codeblock}
{: go}

--->
The options for `{accountFilters}` are: `include_all`, `category_filters`, and `id_filters`.

See the [Catalog Management API](/apidocs/resource-catalog/private-catalog?code=curl#update-catalog-account){: external} for more information.

## Managing access to products for specific users by using the API
{: #set-private-filters-api}
{: api}

Set filters at a private catalog level for fine-grained control of which products in the public catalog are available only to the users you choose. The following example applies the filter `id_filters` where `AdvancedMobileAccess-d6aece47-d840-45b0-8ab9-ad15354deeea` is a product ID.

```bash
curl -X 'PUT' \
'https://cm.globalcatalog.cloud.ibm.com/api/v1-beta/catalogs/<catalog-id>'
 -H 'accept: application/json' \
 -H 'Content-Type: application/json' \
 -H "Authorization: ${IC_IAM_TOKEN}" \
 -d '{"label": "testcurlcatalog4", "short_description": "testing creating a catalog through curl", "catalog_filters": { "include_all": false, "id_filters": { "include": { "filter_terms": [ "AdvancedMobileAccess-d6aece47-d840-45b0-8ab9-ad15354deeea" ] } } }}'
```
{: codeblock}

See the [Catalog Management API](https://cloud.ibm.com/apidocs/resource-catalog/private-catalog?code=curl#replace-catalog){: external} for more information.

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
| Developer tools | Products that support developing, testing, and debugging software. |
| Integration | Products that facilitate the connection of data, apps, APIs, and devices across an organization to be more efficient, productive, and agile. |
| Internet of Things | Products that support receiving and transferring data over wireless networks without human intervention. |
| Logging and monitoring | Products that support receiving and transferring data over wireless networks without human intervention. |
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
| Financial Services Validated | Services are designated as Financial Services Validated when the {{site.data.keyword.cloud_notm}} service or SaaS, or independent software vendor (ISV) offering, evidences compliance with the {{site.data.keyword.cloud_notm}} Framework for Financial Services. |
| HIPAA Enabled | The service is designated as HIPAA ready, meaning processing, storing, and handling Protected Health Information (PHI) in the service is supported. |
| IAM-enabled | The service is enabled to use {{site.data.keyword.cloud_notm}} Identity and Access Management (IAM) for access control. Access policies are used to assign users and service IDs access to specific resources in an account.|
| Service Endpoint Supported | The service can be connected to over the {{site.data.keyword.cloud_notm}} private network instead of the public network. Connecting directly to service endpoints doesn't require internet access, providing increased security. |
{: caption="Table 1. Options for filtering by compliance" caption-side="top"}
{: #compliance-custom}
{: tab-title="Compliance"}
{: tab-group="customcatalogfilters"}
{: class="simple-tab-table"}
{: summary="Use the buttons before the table to change the context of the table. The column headers identify the options for fitering based on filter type."}

| Option | Description |
|--------------|-------|
| Cloud Paks | A cloud solution that integrates a container platform, containerized {{site.data.keyword.IBM_notm}} middleware and open source components, and common software services for development and management. |
| Helm charts | A format for packaging a collection of files that describe specific configurations of infrastructure in the form of code.   |
| Operators | A method of packaging and deploying a Kubernetes-native application. |
| OVA Images | Open Virtual Appliance that contains a compressed installable version of a virtual machine. |
| Server Images | A template that is used to create instances of virtual servers. |
| Terraform |  Infrastructure as code to deploy your application. |
{: caption="Table 1. Options for filtering by delivery method" caption-side="top"}
{: #software-custom}
{: tab-title="Delivery method"}
{: tab-group="customcatalogfilters"}
{: class="simple-tab-table"}
{: summary="Use the buttons before the table to change the context of the table. The column headers identify the options for fitering based on filter type."}

| Option | Description |
|--------------|-------|
| IBM {{site.data.keyword.containershort}} | Used to create a Kubernetes cluster of compute hosts to deploy and manage containerized apps on {{site.data.keyword.cloud_notm}}. |
| {{site.data.keyword.bplong_notm}} | Used for infrastructure as code automation by using terraform templates. |
| {{site.data.keyword.powerSys_notm}} | Used to create a Power server that is distinct from the {{site.data.keyword.cloud_notm}} servers with separate networks and direct-attached storage. The internal networks are fenced but offer connectivity options to  {{site.data.keyword.cloud_notm}} infrastructure or on-premises environments. |
| Red Hat OpenShift | Used to create a {{site.data.keyword.openshiftshort}} cluster of compute hosts to deploy and manage containerized apps on {{site.data.keyword.cloud_notm}}. |
| VMware vCenter Server | Provides deployment and management of VMware virtualized environments. |
| Virtual Private Cloud | Deploy and manage your server images on virtual private cloud as your infrastructure target. |
{: caption="Table 1. Options for filtering by deployment target" caption-side="top"}
{: #swdeploymenttargetfilters}
{: tab-title="Deployment target"}
{: tab-group="customcatalogfilters"}
{: class="simple-tab-table"}
{: summary="Use the buttons before the table to change the context of the table. The column headers identify the options for fitering based on filter type."}

| Option | Description |
|--------------|-------|
| Free | The service includes monthly free allowances for only Pay-As-You-Go or Subscription accounts. |
| Lite | The pricing plan for the service is structured as a free quota. The quota might operate for a specific time period, for example, a month or on a one-off usage basis. |
{: caption="Table 1. Options for filtering by pricing plan" caption-side="top"}
{: #pricingplan-svc}
{: tab-title="Pricing plan"}
{: tab-group="customcatalogfilters"}
{: class="simple-tab-table"}
{: summary="Use the buttons before the table to change the context of the table. The column headers identify the options for fitering based on filter type."}

| Option | Description |
|--------------|-------|
| Beta | The product is available for evaluation and testing purposes. Beta products are not intended for production use. |
| Deprecated | The product is supported but no longer recommended and that might become obsolete. |
{: caption="Table 1. Options for filtering by release" caption-side="top"}
{: #release-custom}
{: tab-title="Release"}
{: tab-group="customcatalogfilters"}
{: class="simple-tab-table"}
{: summary="Use the buttons before the table to change the context of the table. The column headers identify the options for fitering based on filter type."}


| Option | Description |
|--------------|-------|
| HPC | Products that enable High Performance Computing (HPC) workloads on {{site.data.keyword.cloud_notm}}. For more information, see [High-performance computing on {{site.data.keyword.cloud_notm}}](https://www.ibm.com/cloud/hpc){: external} |
| SAP Certified | An infrastructure service that is certified by SAP to run production SAP workloads. For more information, see [{{site.data.keyword.ibm_cloud_sap}}](/docs/sap).|
| Satellite Enabled | A service that is enabled for use with {{site.data.keyword.cloud_notm}} Satellite. You can run apps consistently across on-premises, edge computing, and public cloud environments. For more information, see [{{site.data.keyword.cloud_notm}} {{site.data.keyword.satelliteshort}}](https://www.ibm.com/cloud/satellite){: external}. |
| Quantum Technologies | A service that is compatible with quantum technologies. For more information, see [{{site.data.keyword.IBM_notm}} Quantum services](http://cloud.ibm.com/quantum){: external}. |
{: caption="Table 1. Options for filtering by runtime environment" caption-side="top"}
{: #works-with-custom}
{: tab-title="Works with"}
{: tab-group="customcatalogfilters"}
{: class="simple-tab-table"}
{: summary="Use the buttons before the table to change the context of the table. The column headers identify the options for fitering based on filter type."}


| Option | Description |
|--------------|-------|
| {{site.data.keyword.IBM_notm}} supported | Products that are supported by {{site.data.keyword.cloud_notm}}. |
| Third party supported | Products that are provided by individual service entities. |
| Community supported | Products that are provided by open source communities. |
{: caption="Table 1. Options for filtering by support type" caption-side="top"}
{: #support-type-custom}
{: tab-title="Support"}
{: tab-group="customcatalogfilters"}
{: class="simple-tab-table"}
{: summary="Use the buttons before the table to change the context of the table. The column headers identify the options for fitering based on filter type."}

You can also scope your view of the catalog by using the **Provider** filter to browse by individual providers, and the **Location** filter to view products available in specific regions.
{: tip}
