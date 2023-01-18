---

copyright:
  years: 2020, 2023
lastupdated: "2023-01-18"

keywords: catalog, restrict visibility, hide product, restrict by user, filter catalog, private catalog, catalog management service, public catalog

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Customizing the {{site.data.keyword.cloud_notm}} catalog and private catalogs for users in your account
{: #restrict-by-user}

Private catalogs provide a way to centrally manage access to products in the {{site.data.keyword.cloud}} catalog and your own catalogs. You can customize the public catalog and your private catalogs to make specific solutions available to users in your account. By doing so, you can ensure that your catalogs are relevant to your business.
{: shortdesc}

Let's say you're an account administrator for your team, and you require access to all products in the {{site.data.keyword.cloud_notm}} catalog. A member of your team is tasked with a specific project, for example, building a voice-enabled chatbot by using {{site.data.keyword.conversationshort}}, {{site.data.keyword.speechtotextshort}}, and {{site.data.keyword.texttospeechshort}}. And, you want them to access only those products in the {{site.data.keyword.cloud_notm}} catalog.

To achieve this, you create one catalog that includes all products in the {{site.data.keyword.cloud_notm}} catalog. Then, you create another catalog that includes only the required products, and you give the team member viewer access to the catalog.

All private catalogs that are in an account inherit filters that are set by the account owner or administrator at the account level. In addition, if the account is a parent account in an {{site.data.keyword.cloud_notm}} enterprise, the filters apply to all child account groups and accounts.
{: tip}

## Before you begin
{: #prereq-restrict}

Make sure you have the [administrator role on the catalog management service](/docs/account?topic=account-account-services#catalog-management-account-management) to complete this task.

Run the following command to install the catalogs management plug-in:
{: cli}

```bash
ibmcloud plugin install catalogs-management
```
{: codeblock}
{: cli}

## Creating a private catalog with all products included by using the console
{: #catalog-all-ui}
{: ui}

Complete the following steps to create a catalog that includes all products in the {{site.data.keyword.cloud_notm}} catalog:

1. Go to **Manage** > **Catalogs**, in the {{site.data.keyword.cloud_notm}} console, and click **Create a catalog**.
1. Select the Product (default) catalog type.
1. Enter a name and description.
1. Make sure the **All products** option is selected, and click **Create**. The availability is based on the filters set at the account level on the [Settings page](https://cloud.ibm.com/content-mgmt/catalog-settings){: external}.
1. Confirm that the catalog includes all products by clicking the catalog name > **Manage filters**. Then, check that **Include all products in the {{site.data.keyword.cloud_notm}} catalog** is selected in **Step 1: Select to include or exclude all products in the {{site.data.keyword.cloud_notm}} catalog**.

## Creating a private catalog with select products included by using the console
{: #catalog-select-ui}
{: ui}

Complete the following steps to create a catalog that includes a specific set of products in the {{site.data.keyword.cloud_notm}} catalog:

1. Go to **Manage** > **Catalogs**, in the {{site.data.keyword.cloud_notm}} console, and click **Create a catalog**.
1. Select the Product (default) catalog type.
1. Enter a name and description.
1. Click **Create**.
1. Click the catalog name > **Manage filters**.
1. Select **Exclude all products in the {{site.data.keyword.cloud_notm}} catalog** in **Step 1: Select to include or exclude all products in the {{site.data.keyword.cloud_notm}} catalog**.
1. Skip step 2, and click **Add** in **Step 3: Add exceptions to the rules**.
1. Make sure **Include** is selected as the condition, and then individually select the products you want users to access. In the case of our example project, you select {{site.data.keyword.conversationshort}}, {{site.data.keyword.speechtotextshort}}, and {{site.data.keyword.texttospeechshort}}.

## Setting the visibility of the {{site.data.keyword.cloud_notm}} catalog by using the console
{: #catalog-off-ui}
{: ui}

Now that you've created your private catalogs, complete the following steps to turn off visibility of the public catalog to all users in your account.

1. Click **Catalogs** in the breadcrumb.
2. Click **Settings**.
3. Set **{{site.data.keyword.cloud_notm}} catalog** to **Off**.
4. Confirm that your filters and settings are correctly applied by going to the public catalog, and expanding the catalog switcher. Only the private catalogs in your account should be displayed in the list.

You can update which products are included or excluded at any time by updating your private catalog's settings.
{: note}

## Authorizing access to private catalogs by using the console
{: #custom-catalog-access-ui}
{: ui}

To authorize users to work with the products in your private catalogs, assign them the [viewer role on the catalog management service](/docs/account?topic=account-account-services#catalog-management-account-management).

## Deleting a private catalog by using the console
{: #delete-private-catalog-ui}
{: ui}

If you delete a private catalog, all of the products within the catalog are deleted as well. Complete the following steps to delete a private catalog:

1. Go to **Manage** > **Catalogs**, in the {{site.data.keyword.cloud_notm}} console, and click **Private catalogs**.
1. Click the **Actions** icon ![Actions icon](../icons/actions-icon-vertical.svg "Actions") for the catalog you want to delete, and select **Delete**.

You can [restore a private catalog](/docs/account?topic=account-resource-reclamation&interface=cli#restore-resource-cli) within 7 days after you delete it.
{: tip}

## Creating a private catalog with all products included by using the CLI
{: #catalog-all-cli}
{: cli}

Complete the following steps to create a catalog that includes all products in the {{site.data.keyword.cloud_notm}} catalog:
1. Target a resource group to create a catalog. You can run the `ibmcloud resource groups` command, and then the `ibmcloud target -g "resource group"` command.
1. Use the following command to create a new private catalog in your account.

   ```bash
   ibmcloud catalog create --name CATALOG [--catalog-description "DESCRIPTION"]
   ```
   {: codeblock}

All the {{site.data.keyword.cloud_notm}} catalog products are visible by default when you create a new private catalog. See the [Catalogs management CLI](https://cloud.ibm.com/docs/cli?topic=cli-manage-catalogs-plugin#prereqs-managecatalogs) for more information.


## Creating a private catalog with select products included by using the CLI
{: #catalog-select-cli}
{: cli}

Complete the following steps to create a catalog that includes a specific set of products in the {{site.data.keyword.cloud_notm}} catalog:
1. Target a resource group to create a catalog. You can run the `ibmcloud resource groups` command, and then the `ibmcloud target -g "resource group"` command.
1. Create a new private catalog in your account using the following command.

   ```bash
   ibmcloud catalog create --name CATALOG [--catalog-description "DESCRIPTION"]
   ```
   {: codeblock}

1. Update the filter to include or exclude a particular product or products and any applicable pricing plans. Make sure to specify your catalog, or the filter will default to the account level. See [Catalogs management CLI](https://cloud.ibm.com/docs/cli?topic=cli-manage-catalogs-plugin#offering-filter) for more command options.

   ```bash
   ibmcloud catalog filter offering --offering PRODUCT-NAME
   ```
   {: codeblock}

## Setting the visibility of the {{site.data.keyword.cloud_notm}} catalog by using the CLI
{: #catalog-off-cli}
{: cli}

By default, the {{site.data.keyword.cloud_notm}} public catalog is visible to all users in the account. You can make products available only to the users you choose by turning off visibility to the {{site.data.keyword.cloud_notm}} catalog and adding the products to your private catalogs. Use the following command to turn off visibility of the public catalog to all users in your account.
```bash
ibmcloud catalog filter hide-ibm-public-catalog
```
{: codeblock}

## Authorizing access to private catalogs by using the CLI
{: #custom-catalog-access-cli}
{: cli}

To authorize users to work with the products in your private catalogs, assign them the [viewer role on the catalog management service](/docs/account?topic=account-account-services#assigning-access-by-using-the-cli).

## Deleting a private catalog by using the CLI
{: #delete-private-catalog-cli}
{: cli}

If you delete a private catalog, all of the products within the catalog are deleted as well. Run the following command to delete a private catalog:

```bash
ibmcloud catalog delete --catalog CATALOG
```
{: codeblock}

You can [restore a private catalog](/docs/account?topic=account-resource-reclamation&interface=cli#restore-resource-cli) within 7 days after you delete it.
{: tip}

## Creating a private catalog with all products included by using the API
{: #catalog-all-api}
{: api}

To create a catalog that includes all products in the {{site.data.keyword.cloud_notm}} catalog, call the [Catalog Management API](https://cloud.ibm.com/apidocs/resource-catalog/private-catalog?code=go#create-catalog) as shown in the following sample request. Replace variables with the values from your account.

```bash
curl -X 'POST' \
'https://cm.globalcatalog.cloud.ibm.com/api/v1-beta/catalogs' \
-H 'accept: application/json' \
-H 'Content-Type: application/json' \
-H "Authorization: ${IC_IAM_TOKEN}" \
-d '{"label": "testcurlcatalog", "short_description": "testing creating a catalog through curl"}'
```
{: codeblock}
{: curl}

```java
ServiceCall<Catalog> createCatalog(CreateCatalogOptions createCatalogOptions)

Example request

String label = "{label}";
String shortDesc = "{shortDesc}";
CreateCatalogOptions createOptions = new CreateCatalogOptions.Builder().label(label).shortDescription(shortDesc).build();
Response<Catalog> response = service.createCatalog(createOptions).execute();
System.out.println(response.getResult());
```
{: java}
{: codeblock}

```node
createCatalog(params, [callback()])

Example request

label = "{label}";
shortDesc = "{shortDesc}";
response = await service.createCatalog({ 'label': label, 'shortDescription': shortDesc });
console.log(response);
```
{: javascript}
{: codeblock}

```python
create_catalog(self, id=None, rev=None, label=None, short_description=None, catalog_icon_url=None, tags=None, url=None, crn=None, offerings_url=None, features=None, disabled=None, created=None, updated=None, resource_group_id=None, owning_account=None, catalog_filters=None, syndication_settings=None, **kwargs)

Exapmle request

label = "{label}"
shortDesc = "{shortDesc}"
response = self.service.create_catalog(label=label, short_description=shortDesc)
print(response)
```
{: python}
{: codeblock}

```go
(catalogManagement *CatalogManagementV1) CreateCatalog(createCatalogOptions *CreateCatalogOptions) (result *Catalog, response *core.DetailedResponse, err error)

Example request

label := "{label}"
shortDesc := "{shortDesc}"
createOptions := service.NewCreateCatalogOptions()
createOptions.SetLabel(label)
createOptions.SetShortDescription(shortDesc)
_, response, _ := service.CreateCatalog(createOptions)
fmt.Println(response)
```
{: go}
{: codeblock}

All the {{site.data.keyword.cloud_notm}} public catalog offerings are visible by default when you create a new private catalog. See the [Catalog Management API](https://cloud.ibm.com/apidocs/resource-catalog/private-catalog?code=java#create-catalog) for more information.

## Creating a private catalog with select products included by using the API
{: #catalog-select-api}
{: api}

To create a catalog that includes a specific set of products in the {{site.data.keyword.cloud_notm}} catalog, call the [Catalog Management API](https://cloud.ibm.com/apidocs/resource-catalog/private-catalog?code=go#create-catalog) as shown in the following sample request. Replace variables with the values from your account.

```bash
curl -X 'POST' \
'https://cm.globalcatalog.cloud.ibm.com/api/v1-beta/catalogs' \
-H 'accept: application/json' \
-H 'Content-Type: application/json' \
-H "Authorization: ${IC_IAM_TOKEN}" \
-d '{"label": "testcurlcatalog4", "short_description": "testing creating a catalog through curl", "catalog_filters": { "include_all": false, "id_filters": { "include": { "filter_terms": [ "AdvancedMobileAccess-d6aece47-d840-45b0-8ab9-ad15354deeea" ] } } }}'
```
{: codeblock}

Make sure to exclude all public catalog products by setting the `include_all` field has a boolean value of `false` for each `catalog_filters` object. To specify the products you want to include you can filter by `category_filters` or `id_filters`. Give `filter_terms` the product property or product ID you want to include. In this example, `AdvancedMobileAccess-d6aece47-d840-45b0-8ab9-ad15354deeea` is a product ID.

See the [Catalog Management API](https://cloud.ibm.com/apidocs/resource-catalog/private-catalog?code=node#replace-catalog) for more command options.

## Setting the visibility of the {{site.data.keyword.cloud_notm}} catalog by using the API
{: #catalog-off-api}
{: api}

To hide the public catalog in an account, make sure the `hide_IBM_cloud_catalog` field has a boolean value of `true`. Alternatively, you can give the `include_all` field a boolean value of `false` for each `account_filters` object. Then only the private catalogs you create should be displayed in your account.

```bash
curl -X "PUT" "https://cm.globalcatalog.cloud.ibm.com/api/v1-beta/catalogaccount"
-H "accept: */*"
-H "Authorization: {iam-bearer-token}"
-d '{"id":"string","hide_IBM_cloud_catalog":true,"account_filters":{"include_all":true,"category_filters":{"additionalProp1":{"include":true,"filter":{"filter_terms":["string"]}},"additionalProp2":{"include":true,"filter":{"filter_terms":["string"]}},"additionalProp3":{"include":true,"filter":{"filter_terms":["string"]}}},"id_filters":{"include":{"filter_terms":["string"]},"exclude":{"filter_terms":["string"]}}}}'
```
{: codeblock}
{: curl}

See the [Catalog Management API](https://cloud.ibm.com/apidocs/resource-catalog/private-catalog#update-catalog-account) for more information.

## Authorizing access to private catalogs by using the API
{: #customcatalog-access-api}
{: api}

To authorize users to work with the products in your private catalogs, assign them the [viewer role on the catalog management service](/docs/account?topic=account-account-services#api-acct-mgmt).

## Deleting a private catalog by using the API
{: #delete-private-catalog-api}
{: api}

If you delete a private catalog, all of the products within the catalog are deleted as well. Use the following command to delete a private catalog:

```bash
DELETE /catalogs/{catalog_identifier}
```
{: codeblock}
{: curl}

See the [Catalog Management API](https://cloud.ibm.com/apidocs/resource-catalog/private-catalog?code=curl#delete-catalog) for more information.

You can [restore a private catalog](/docs/account?topic=account-resource-reclamation&interface=api#restore-resource-api) within 7 days after you delete it.
{: tip}

## Creating a private catalog by using Terraform
{: #catalog-all-terraform}
{: terraform}

Before you can create a private catalog by using Terraform by using Terraform, make sure that you have completed the following:

- Install the Terraform CLI and configure the {{site.data.keyword.cloud_notm}} Provider plug-in for Terraform. For more information, see the tutorial for [Getting started with Terraform on {{site.data.keyword.cloud}}](/docs/ibm-cloud-provider-for-terraform?topic=ibm-cloud-provider-for-terraform-getting-started). The plug-in abstracts the {{site.data.keyword.cloud_notm}} APIs that are used to complete this task.
- Create a Terraform configuration file that is named `main.tf`. In this file, you add the configuration to create an authorization between services by using HashiCorp Configuration Language. For more information, see the [Terraform documentation](https://www.terraform.io/docs/language/index.html){: external}.

You cannot customize the public catalog and your private catalogs to make specific solutions available to users in your account by using Terraform. To customize the public catalog and your private catalogs, switch to the UI, CLI, or API steps.
{: important}

Use the following steps to create a private catalog:

1. Create an argument in your `main.tf` file. The following example creates a catalog by using the `ibm_cm_catalog` resource, where `label` is a display name to identify the catalog.

   ```terraform
   resource "ibm_cm_catalog" "cm_catalog" {
   label = "label"
   short_description = "short_description"
   }
   ```
   {: codeblock}

   For more information, see the argument reference details on the [Terraform Catalog Management](https://registry.terraform.io/providers/IBM-Cloud/ibm/latest/docs/resources/cm_catalog){: external} page.

1. After you finish building your configuration file, initialize the Terraform CLI. For more information, see [Initializing Working Directories](https://www.terraform.io/cli/init){: external}.

   ```terraform
   terraform init
   ```
   {: pre}

1. Provision the resources from the `main.tf` file. For more information, see [Provisioning Infrastructure with Terraform](https://www.terraform.io/cli/run){: external}.

   1. Run `terraform plan` to generate a Terraform execution plan to preview the proposed actions.

      ```terraform
      terraform plan
      ```
      {: pre}

   1. Run `terraform apply` to create the resources that are defined in the plan.

      ```terraform
      terraform apply
      ```
      {: pre}

## Authorizing access to private catalogs by using Terraform
{: #customcatalog-access-terraform}
{: terraform}

To authorize users to work with the products in your private catalogs, assign them the [viewer role on the catalog management service](/docs/account?topic=account-account-services&interface=terraform#api-acct-mgmt).
