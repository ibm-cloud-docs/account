---

copyright:

  years: 2020, 2023
lastupdated: "2023-12-15"

keywords: account resources, delete resource, delete instance

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Deleting resources
{: #delete-resource}

When you don't need a resource in your account anymore, or if a user in your account created a resource that you don't want them to use, you can delete the instance from your account.
{: shortdesc}

## Deleting resources in the console
{: #delete-resource-console}
{: ui}

You can delete a resource in the console by using the following steps:

1. From the {{site.data.keyword.cloud}} console, click the **Navigation Menu** icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Resource list** to view your list of resources.
2. Expand the sections to locate the service instance that you want to delete.
3. Click the **Actions** icon ![Actions icon](../icons/action-menu-icon.svg) > **Delete** for the row.

## Deleting resources by using the CLI
{: #delete-resource-cli}
{: cli}

You can delete a resource by using the {{site.data.keyword.Bluemix}} Command Line Interface. For detailed information about managing IBM Cloud resources, see [Working with resources and resource groups](/docs/cli?topic=cli-ibmcloud_commands_resource).

1. Log in, and select the account.

   ```bash
   ibmcloud login
   ```
   {: codeblock}

2. Delete a service instance by running the [`ibmcloud resource service-instance-delete`](/docs/cli?topic=cli-ibmcloud_commands_resource#ibmcloud_resource_service_instance_delete) command, where `NAME` is the name of the service instance, exclusive with ID, and `ID` is the ID of the service instance, exclusive with NAME.

   ```bash
   ibmcloud resource service-instance-delete (NAME|ID) [-f, --force] [--recursive]
   ```
   {: codeblock}

   For example, the following command deletes a resource service-instance that's named `my-service-instance`:

   ```bash
   ibmcloud resource service-instance-delete my-service-instance
   ```
   {: codeblock}

## Deleting resource instances by using the API
{: #delete-resource-instance-api}
{: api}

You can programmatically delete a resource instance by calling the Resource Controller API as shown in the following sample request. For detailed information about the API, see [Resource Controller API](https://cloud.ibm.com/apidocs/resource-controller/resource-controller#delete-resource-instance){: external}.

```bash
curl -X DELETE \
https://resource-controller.cloud.ibm.com/v2/resource_instances/8d7af921-b136-4078-9666-081bd8470d94 \
  -H 'Authorization: Bearer <>'
```
{: pre}
{: curl}

```java
DeleteResourceInstanceOptions deleteResourceInstanceOptions = new DeleteResourceInstanceOptions.Builder()
  .id(instanceGuid)
  .recursive(false)
  .build();

Response<Void> response = service.deleteResourceInstance(deleteResourceInstanceOptions).execute();

System.out.printf("deleteResourceInstance() response status code: %d\n", response.getStatusCode());
```
{: codeblock}
{: java}

```javascript
const params = {
  id: instanceGuid,
  recursive: false,
};

resourceControllerService.deleteResourceInstance(params)
  .then(res => {
    console.log('deleteResourceInstance() response status code: ' + res.status);
  })
  .catch(err => {
    console.warn(err)
  });
```
{: codeblock}
{: javascript}

```python
response = resource_controller_service.delete_resource_instance(
    id=instance_guid,
    recursive=False
)

print('\ndelete_resource_instance() response status code: ',
      response.get_status_code())
```
{: codeblock}
{: python}

```go
deleteResourceInstanceOptions := resourceControllerService.NewDeleteResourceInstanceOptions(
  instanceGUID,
)
deleteResourceInstanceOptions.SetRecursive(false)

response, err := resourceControllerService.DeleteResourceInstance(deleteResourceInstanceOptions)
if err != nil {
  panic(err)
}
fmt.Printf("\nDeleteResourceInstance() response status code: %d\n", response.StatusCode)
```
{: codeblock}
{: go}

## Deleting resource instances by using Terraform
{: #delete-resource-instance-terraform}
{: terraform}

Use the following steps to delete resource instances by using Terraform.

1. You can delete a resource instance by removing the following code block from your terraform file. You must have created the `resource_instance` using the terraform file.

   ```terraform
   data "ibm_resource_group" "group" {
   name = "test"
   }

   resource "ibm_resource_instance" "resource_instance" {
    name              = "test"
    service           = "cloud-object-storage"
    plan              = "lite"
    location          = "global"
    resource_group_id = data.ibm_resource_group.group.id
    tags              = ["tag1", "tag2"]

    //User can increase timeouts
    timeouts {
    create = "15m"
    update = "15m"
    delete = "15m"
    }
   }
   ```
   {: codeblock}

   For more information, see the argument reference details on the [Terraform Resource Management](https://registry.terraform.io/providers/IBM-Cloud/ibm/latest/docs/resources/resource_instance){: external} page.

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


You can also delete a resource instance by running the following `terraform destroy` command.

```terraform
terraform destroy -target RESOURCE_TYPE.NAME -target RESOURCE_TYPE2.NAME
```
{: pre}
