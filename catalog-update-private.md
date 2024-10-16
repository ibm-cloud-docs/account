---

copyright:
  years: 2020, [{CURRENT_YEAR}]
lastupdated: "2024-01-05"

keywords: catalog, private catalog, update, private catalog product, update version, versions

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Updating your software
{: #update-private}

To update the software that's in your private catalog, you can add a new version or update and republish an existing version.
{: shortdesc}

## Before you begin
{: #prereq-update}

To complete this task, you need to be assigned the editor role on the catalog management service. For more information, see [Assigning users access](/docs/account?topic=account-catalog-access).

To update your software by using Terraform, make sure that you have completed the following:
{: terraform}

- Install the Terraform CLI and configure the {{site.data.keyword.cloud_notm}} Provider plug-in for Terraform. For more information, see the tutorial for [Getting started with Terraform on {{site.data.keyword.cloud}}](/docs/ibm-cloud-provider-for-terraform?topic=ibm-cloud-provider-for-terraform-getting-started). The plug-in abstracts the {{site.data.keyword.cloud_notm}} APIs that are used to complete this task.
- Create a Terraform configuration file that is named `main.tf`. In this file, you define resources by using HashiCorp Configuration Language. For more information, see the [Terraform documentation](https://developer.hashicorp.com/terraform/language){: external}.
{: terraform}

## Update an existing version by using the console
{: #update-editor-offering}
{: ui}

The following steps walk through an example of making updates to a product's readme file to show the complete process for updating an existing software version.

1. In the {{site.data.keyword.cloud}} console, go to **Manage** > **Catalogs** > **Private catalogs**, and select your catalog from the list.
1. Click the name of your software product.
1. Select **Private products** to navigate to the list of products that are in your private catalog.
1. Click the **Actions** icon ![Actions icon](../icons/actions-icon-vertical.svg "Actions"), and select **Edit**.
1. Click the Edit readme tab.
1. Click the **Edit** icon ![Edit icon](../icons/icon_write.svg "Edit"), add a new line of text to the Introduction section, and click **Update**.
1. Click the **Actions** icon ![Actions icon](../icons/actions-icon-vertical.svg "Actions"), and select **Merge changes** to publish the updated version to your account.

## Update an existing version by using the CLI
{: #update-version-cli}
{: cli}

Complete the following steps to create a draft version, update it, and merge the changes to the current version of your software.

   You need the version locator for your software. To find it, run the **`ibmcloud catalog offering list --catalog "your-private-catalog"`** command and search for the existing version number.
   {: important}

1. Create a draft version of your software.
    ```bash
    ibmcloud catalog offering create-draft --version-locator <VERSION_LOCATOR>
    ```
    {: codeblock}

1. Set another category.
    ```bash
    ibmcloud catalog offering add-category --catalog "your-private-catalog" --offering "your-software" --category "category-type"
    ```
    {: codeblock}

1. Merge the draft update to your software. This action merges the update to the version of your software that's published in your account.
    ```bash
    ibmcloud catalog offering merge-draft --version-locator **<VERSION_LOCATOR_OF_DRAFT_VERSION>**
    ```
    {: codeblock}

1.  Search for the software in the {{site.data.keyword.cloud_notm}} catalog.
    ```bash
    ibmcloud catalog get --public | grep your-software
    ```
    {: codeblock}

## Update an existing version by using the API
{: #update-version-api}
{: api}

You can programmatically update a version by calling the Catalog Management API as shown in the following sample request. For detailed information about the API, see [Catalog Management API](https://cloud.ibm.com/apidocs/resource-catalog/private-catalog?code=python#replace-offering){: external}.

```java
String catalogID = "{catalogID}";
String offeringID = "{offeringID}";
String label = "{label}";
String shortDesc = "{shortDesc}";
ReplaceOfferingOptions replaceOptions = new ReplaceOfferingOptions.Builder().catalogIdentifier(catalogID).id(offeringID).offeringId(offeringID).label(label).shortDescription(shortDesc).rev(revision.rev()).build();
Response<Catalog> response = service.replaceOffering(replaceOptions).execute();
System.out.println(response.getResult());
```
{: codeblock}
{: java}

```javascript
vcatalogID = "{catalogID}";
offeringID = "{offeringID}";
revision = "{revision}";
label = "{label}";
shortDesc = "{shortDesc}";
response = await service.replaceOffering({'catalogIdentifier': catalogID, 'offeringId': offeringID, 'id': offeringID, 'rev': revision, 'label': label, 'shortDescription': shortDesc});
console.log(response);
```
{: codeblock}
{: javascript}

```python
catalogID = "{catalogID}"
offeringID = "{offeringID}"
revision = "{revision}"
shortDesc = "{shortDesc}"
response = self.service.replace_offering(catalog_identifier=catalogID, offering_id=offeringID, id=offeringID, rev=revision, label=label, short_description=shortDesc)
print(response)
```
{: codeblock}
{: python}

```go
catalogID := "{catalogID}"
offeringID := "{offeringID}"
label := "{label}"
shortDesc := "{shortDesc}"
revision := "{revision}"
updateOptions := service.NewReplaceOfferingOptions(catalogID, offeringID)
updateOptions.SetID(offeringID)
updateOptions.SetLabel(label)
updateOptions.SetShortDescription(shortDesc)
updateOptions.SetRev(revision)
_, response, _ := service.ReplaceOffering(updateOptions)
fmt.Println(response)
```
{: codeblock}
{: go}

## Update an existing version by using Terraform
{: #update-editor-terraform}
{: terraform}

Use the following steps to update an existing version of your software by using Terraform.

1. Create an argument in your `main.tf` file. The following example accesses the software version by using the `cm_version` resource, where `offering_id` identifies the software.

   ```terraform
   resource "cm_version" "cm_version" {
   catalog_identifier = "catalog_identifier"
   offering_id = "offering_id"
   zipurl = "zipurl"
   }
   ```
   {: codeblock}

   For more information, see the argument reference details on the [Terraform Catalog Management](https://registry.terraform.io/providers/IBM-Cloud/ibm/latest/docs/resources/cm_version){: external} page.

1. After you finish building your configuration file, initialize the Terraform CLI. For more information, see [Initializing Working Directories](https://developer.hashicorp.com/terraform/cli/init){: external}.

   ```terraform
   terraform init
   ```
   {: pre}

1. Provision the resources from the `main.tf` file. For more information, see [Provisioning Infrastructure with Terraform](https://developer.hashicorp.com/terraform/cli/run){: external}.

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
