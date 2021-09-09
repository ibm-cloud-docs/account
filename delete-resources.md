---



copyright:

  years: 2020, 2021
lastupdated: "2021-08-31"

keywords: account resources, delete resource, delete instance

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:curl: .ph data-hd-programlang='curl'}
{:go: .ph data-hd-programlang='go'}
{:javascript: .ph data-hd-programlang='javascript'}
{:java: .ph data-hd-programlang='java'}
{:python: .ph data-hd-programlang='python'}
{:ruby: .ph data-hd-programlang='ruby'}
{:ui: .ph data-hd-interface='ui'}
{:cli: .ph data-hd-interface='cli'}
{:api: .ph data-hd-interface='api'}
{:terraform: .ph data-hd-interface='terraform'}

# Deleting resources 
{: #delete-resource}

When you don't need a resource in your account anymore, or if a user in your account created a resource that you don't want them to use, you can delete the instance from your account.
{: shortdesc}

## Deleting resources in the console
{: #delete-resource-console}
{: ui}

You can delete a resource in the console by using the following steps:

1. From your dashboard, click **View resources** in the Resources summary widget.
2. Expand the sections to locate the service instance that you want to delete.
3. Click the **Actions** icon ![Actions icon](../icons/action-menu-icon.svg) > **Delete** for the row.

## Deleting resources by using the CLI
{: #delete-resource-cli}
{: cli}

You can delete a resource by using the {{site.data.keyword.Bluemix}} Command Line Interface. For detailed information about managing IBM Cloud resources, see [Working with resources and resource groups](/docs/cli?topic=cli-ibmcloud_commands_resource).

1. Log in, and select the account.

   ```
   ibmcloud login
   ```
   {: codeblock}

2. Delete a service instance by running the [`ibmcloud resource service-instance-delete`](/docs/cli?topic=cli-ibmcloud_commands_resource#ibmcloud_resource_service_instance_delete) command, where `NAME` is the name of the service instance, exclusive with ID, and `ID` is the ID of the service instance, exclusive with NAME.

   ```
   ibmcloud resource service-instance-delete (NAME|ID) [-f, --force] [--recursive]
   ```
   {: codeblock}
   
   For example, the following command deletes a resource service-instance that's named `my-service-instance`:
   
   ```
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

You can delete a resource instance by using Terraform. 

1. To install the Terraform CLI and configure the {{site.data.keyword.cloud_notm}} Provider plug-in for Terraform, follow the tutorial for [Getting started with Terraform on {{site.data.keyword.cloud}}](/docs/ibm-cloud-provider-for-terraform?topic=ibm-cloud-provider-for-terraform-getting-started). The plug-in abstracts the {{site.data.keyword.cloud_notm}} APIs that are used to complete this task.

2. Create a Terraform configuration file that is named `main.tf`. In this file, you add the configuration to delete a resource instance by using HashiCorp Configuration Language. For more information, see the [Terraform documentation](https://www.terraform.io/docs/language/index.html){: external}.

3. You can delete a resource instance by removing the following code block from your terraform file. You must have provisioned the `resource_instance` using the terraform file.

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
  
4. Initialize the Terraform CLI.

   ```
   terraform init
   ```
   {: pre}
   
5. Create a Terraform execution plan. The Terraform execution plan summarizes all the actions that need to be run to delete a resource instance.

   ```
   terraform plan
   ```
   {: pre}

6. Delete the resource instance.

   ```
   terraform apply
   ```
    
You can also delete a resource instance by running the following `terraform destroy` command.

```
terraform destroy -target RESOURCE_TYPE.NAME -target RESOURCE_TYPE2.NAME
```

