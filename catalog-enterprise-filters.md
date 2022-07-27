---

copyright:
  years: 2020, 2022
lastupdated: "2022-02-18"

keywords: catalog, private catalog, catalog management service, public catalog, enterprise account, child account, account group, enterprise, IBM Cloud catalog

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}


# Customizing the {{site.data.keyword.cloud_notm}} catalog for an enterprise
{: #catalog-enterprise-restrict}

As the account owner or administrator, you can manage which products in the {{site.data.keyword.cloud}} catalog are available for your enterprise. You can choose to include all products, a set of products, or only certain products. You can also specify what level of the enterprise hierarchy the filters apply to. And, you can further restrict which products are available for a specific account group or account. 
{: shortdesc}

## Before you begin
{: #catalog-enterprise-prereqs}

* [Set up your enterprise](/docs/account?topic=account-enterprise-tutorial).
* Make sure you have the [administrator role on the catalog management service](/docs/account?topic=account-account-services#catalog-management-account-management).

## Managing products at the enterprise level
{: #catalog-enterprise-filter}
{: ui}

Centrally manage what's available in the catalog for your entire enterprise hierarchy by setting filters at the enterprise level. The filters automatically apply to all child account groups and accounts. 

Let's say your organization is tasked with implementing a development and deployment model that's focused on improved speed, quality, and control. You might choose to restrict the catalog to only {{site.data.keyword.IBM_notm}} products that are related to DevOps technologies for all members in your enterprise. 

1. Go to **Manage** > **Catalogs** > **Settings** in the {{site.data.keyword.cloud_notm}} console.
2. Select **Exclude all products in the {{site.data.keyword.cloud_notm}} catalog**.
3. Select one or more filters to customize which products are available. In the case of our example, select the following filters: 

   * **Category** > **Developer tools**
   * **Provider** > **{{site.data.keyword.IBM_notm}}**
4. Review the **Preview** table to confirm your selections, and click **Update**. 
5. Verify your updates in the catalog by going to **Catalog** > **Services**.
6. Expand the list of accounts in the console menu bar and select a child account to verify the catalog includes only the products you selected. 
{: ui}

## Managing products for child account groups and accounts
{: #catalog-enterprise-child}
{: ui}

To build on the example in the previous section, all account groups and accounts in your enterprise have access to Developer tools products provided by {{site.data.keyword.IBM_notm}}. You can further restrict access to a subset of products for child account groups and accounts. For example, you might want to limit a specific account group, and its child accounts, to work with only the products that support IAM for access control. 

1. Go to **Manage** > **Catalogs** > **Settings** in the {{site.data.keyword.cloud_notm}} console.
2. Expand the enterprise hierarchy, and select the specific account group. 
3. Select **Exclude all products in the {{site.data.keyword.cloud_notm}} catalog**.
4. Select **Compliance** > **IAM-enabled**. 
5. Review the **Preview** table to confirm your selections, and click **Update**. 
6. Switch to a child account in the account group by selecting it from the list of accounts in console menu bar. 
7. Verify your updates in the catalog by going to **Catalog** > **Services**.
{: ui}

## Managing products at the enterprise level by using the CLI
{: #cli-catalog-enterprise-restrict}
{: cli}

This action can be done only in the console or through the API or SDKs. To see the steps, switch to the **UI** or **API** instructions.

## Managing products for child account groups and accounts by using the CLI
{: #cli-child-account-groups}
{: cli}

You can restrict access to a subset of products for child account groups and accounts. For example, within your enterprise you might want to limit a specific account group, and its child accounts, to work with only the products that support IAM for access control. 

1. Create a new filter.

   ```bash
   ibmcloud catalog filter create [--catalog CATALOG] [--category CATEGORY] [--compliance COMPLIANCE] [--deployment-target TARGET] [--exclude-list LIST] [--include-all ALL] [--include-list LIST] [--offering-format FORMAT] [--pricing-plan PLAN] [--provider PROVIDER] [--release RELEASE] [--type TYPE]
   ```
   {: codeblock}

   If you don't specify the `--catalog CATALOG` command, the filter is created at the account level.
   {: note}

1. Target an account group by specifying the command option `--account-group ACCOUNT GROUP`.
1. Update the filter to include or exclude a particular product or products. See the [Catalog management CLI](https://cloud.ibm.com/docs/cli?topic=cli-manage-catalogs-plugin#create-filter) guidance for command options or run the `ibmcloud catalog filter options` command to retrieve the filter options for each filter category.


## Managing products at the enterprise level by using the API
{: #catalog-enterprise-filter-api}
{: api}

Centrally manage what's available in the catalog for your entire enterprise hierarchy by setting filters at the enterprise level. The filters automatically apply to all child account groups and accounts.

```java
String id = "{id}";
String revision = "{revision}";
String accountFilters = {accountFilters};
ReplaceCatalogOptions replaceOptions = new ReplaceEnterpriseOptions.Builder().enterpriseId(id).id(id).rev(revision).accountFilters(accountFilters).build();
Response<Catalog> response = service.replaceEnterprise(replaceOptions).execute();
System.out.println(response.getResult());
```
{: codeblock}
{: java}

```javascript
id = "{id}";
revision = "{revision}";
accountFilters = {accountFilters};
response = await service.replaceEnterprise({ 'enterpriseId': id, 'id': id, 'rev': revision, 'accountFilters': accountFilters, });
console.log(response);
```
{: codeblock}
{: javascript}

```python
id = "{id}"
revision = "{revision}"
accountFilters = "{accountFilters}"
response = self.service.replace_enterprise(enterprise_id=id, id=id, rev=revision, account_filters= accountFilters)
print(response)
```
{: codeblock}
{: python}

```go
id := "{id}"
revision := "{revision}"
accountFilters := {accountFilters}
replaceOptions := {replaceOptions}
replaceOptions := service.NewReplaceEnterpriseOptions(id)
replaceOptions.SetID(id)
replaceOptions.SetRev(revision)
replaceOptions.SetAccountFilters(accountFilters)
response, _ := service.ReplaceEnterprise(replaceOptions)
fmt.Println(response)
```
{: codeblock}
{: go}

## Managing products for child account groups and accounts by using the API
{: #api-catalog-enterprise-restrict}
{: api}

You can restrict access to a subset of products for child account groups and accounts. For example, within your enterprise you might want to limit a specific account group, and its child accounts, to work with only the products that support IAM for access control. 

The following example request restricts the products for an account group and child accounts. When you call the API, replace the ID variables with the values that are specific to your target account group or account. The options for `{account_filters}` are: `inculde_all`, `category_filters`, and `id_filters`.

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
