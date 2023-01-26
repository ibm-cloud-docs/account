---



copyright:

  years: 2020, 2023
lastupdated: "2023-01-18"

keywords: delete resource group, resource group, manage resource groups

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}


# Deleting a resource group
{: #delete_rgs}

You can't delete the default resource group that's added to your account. Besides the default one, you can only delete a resource group if it doesn't contain any resources.
{: shortdesc}

## Deleting a resource group in the console
{: #delete-rg-console}
{: ui}

To delete a resource group that doesn't contain resources and is not your default, complete the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, go to **Manage** > **Account** > **Account resources** > **Resource groups**.
2. Click the **Actions** icon ![Actions icon](../icons/action-menu-icon.svg "Actions") > **Delete**.

## Deleting a resource group by using the CLI
{: #delete-rg-cli}
{: cli}

To delete a resource group that doesn't contain resources and is not your default, run the [`ibmcloud resource group-delete`](/docs/cli?topic=cli-ibmcloud_commands_resource#ibmcloud_resource_group_delete). For example, delete resource group `example-group`:

```bash
ibmcloud resource group-delete example-group -f
```
{: codeblock}

## Deleting a resource group by using the API
{: #delete-rg-api}
{: api}

You can programmatically delete a resource group by calling the Resource Manager API as shown in the following sample request. For detailed information about the API, see [Resource Manager API](https://cloud.ibm.com/apidocs/resource-controller/resource-manager#delete-resource-group){: external}.

```bash
curl -X DELETE \
  https://resource-controller.cloud.ibm.com/v2/resource_groups/09f8c1c0742c493f80baaf7835212345 \
  -H 'Authorization: Bearer <IAM_TOKEN>'
  -H 'Content-Type: application/json'
```
{: pre}
{: curl}

```java
String id = '09f8c1c0742c493f80baaf7835212345';
DeleteResourceGroupOptions options = new DeleteResourceGroupOptions.Builder().id(id).build();
Response<Void> response = service.deleteResourceGroup(options).execute();
System.out.println(response):
```
{: codeblock}
{: java}

```javascript
const params = {
    id: '09f8c1c0742c493f80baaf7835212345'
};
service.deleteResourceGroup(params).then(response => {
    console.log(response)
}).catch(err => {});
```
{: codeblock}
{: javascript}

```python
delete_resource_group(self,
        id: str,
        **kwargs
    ) -> DetailedResponse
 ```
{: codeblock}
{: python}

```go
ID := "09f8c1c0742c493f80baaf7835212345"
deleteResourceGroupOptionsModel := service.NewDeleteResourceGroupOptions(ID)
detailedResponse, err := service.DeleteResourceGroup(deleteResourceGroupOptionsModel)
```
{: codeblock}
{: go}

## Deleting a resource group by using Terraform
{: #delete-rg-terraform}
{: terraform}

Before you can delete a resource group by using Terraform, make sure that you have completed the following:

- Install the Terraform CLI and configure the {{site.data.keyword.cloud_notm}} Provider plug-in for Terraform. For more information, see the tutorial for [Getting started with Terraform on {{site.data.keyword.cloud}}](/docs/ibm-cloud-provider-for-terraform?topic=ibm-cloud-provider-for-terraform-getting-started). The plug-in abstracts the {{site.data.keyword.cloud_notm}} APIs that are used to complete this task.
- Create a Terraform configuration file that is named `main.tf`. In this file, you define resources by using HashiCorp Configuration Language. For more information, see the [Terraform documentation](https://www.terraform.io/docs/language/index.html){: external}.

Use the following steps to delete a resource group:

The resource group can be deleted only if there are no resources in it.
{: note}

1. You can delete the resource group by removing the following code block from your Terraform `main.tf` file. You must have created the `resourceGroup` using the Terraform file.

   ```terraform
   resource "ibm_resource_group" "resourceGroup" {
    name     = "prod"
   }
   ```
   {: codeblock}

   For more information, see the argument reference details on the [Terraform Resource Management](https://registry.terraform.io/providers/IBM-Cloud/ibm/latest/docs/resources/resource_group){: external} page.

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

You can also delete a resource group by running the following `terraform destroy` command.

```terraform
terraform destroy -target RESOURCE_TYPE.NAME -target RESOURCE_TYPE2.NAME
```
{: pre}
