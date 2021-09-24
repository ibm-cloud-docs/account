---



copyright:

  years: 2019, 2021
lastupdated: "2021-09-24"

keywords: resource, account resources, create resource, access to create resources

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:term: .term}
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

# Creating resources 
{: #manage_resource}

A [resource](x2004267){: term} is anything that you can create from the catalog that is managed by and contained within a resource group. You can create and manage resources by going to your [resource list](https://cloud.ibm.com/resources) in the {{site.data.keyword.cloud}} console or by using the command-line interface (CLI).
{: shortdesc}

Services that are managed by using {{site.data.keyword.Bluemix_notm}} [Identity and Access Management (IAM) access control](/docs/account?topic=account-userroles) and belong to a resource group have several benefits. Some of the benefits include the ability to connect to apps and services in any Cloud Foundry space, which means you can connect apps and services from different locations. Because resource groups are not scoped by location, you can provision apps and services from different locations into the same resource group. You can also use fine-grained access control down to an individual instance within a resource group.

Not all services support the use of resource groups and IAM currently. All service instances that are added to Cloud Foundry orgs and spaces when they're created from the catalog are distinctly different from IAM-enabled services. These services are called Cloud Foundry services. Cloud Foundry services have no connection to resource groups and use [Cloud Foundry roles for access management](/docs/account?topic=account-cfaccess). As services enable support for IAM and resource groups, you're notified about the ability to [migrate existing Cloud Foundry instances to a resource group](/docs/account?topic=account-migrate).

## Required access for creating resources
{: #creating-resources}

For users in your account to be able to create resources from the catalog and assign them to a resource group, they must be assigned two access policies:

* A policy with viewer role or higher on the resources group itself
* A policy with editor role or higher on the service in the account

## Creating resources in the console
{: #create-resource-console}
{: ui}

Use the following steps to create a resource in the console: 
1. From your dashboard, click **View resources** within the Resources summary widget.
2. Click **Create resource**. From here, you are directed to the catalog. You can search the offerings or filter based on a specific category, provider, pricing plan, type of compliance, or release type. Examples of resources include apps, service instances, container clusters, storage volumes, virtual servers, and software. 

After you create the resource, it is displayed in your list of resources on the Resource list page.

## Creating resources by using the CLI
{: #create-resource-cli}
{: cli}

You can create a resource by using the {{site.data.keyword.Bluemix}} Command Line Interface. For more information, see [Working with resources and resource groups](/docs/cli?topic=cli-ibmcloud_commands_resource).

1. Log in, and select the account.

   ```bash
   ibmcloud login
   ```
   {: codeblock}

2. Create an organization by running the [`ibmcloud resource service-instance-create`](https://cloud.ibm.com/docs/cli?topic=cli-ibmcloud_commands_resource#ibmcloud_resource_service_instance_create) command.
In this command `NAME` is the name of the service instance, `SERVICE_NAME or SERVICE_ID` is the name or ID of the service, `SERVICE_PLAN_NAME or SERVICE_PLAN_ID`is the name or ID of the service plan, and ` LOCATION`is the target location or environment to create the service instance.

   ```bash
   ibmcloud resource service-instance-create NAME (SERVICE_NAME | SERVICE_ID) SERVICE_PLAN_NAME LOCATION [-d, --deployment DEPLOYMENT_NAME] [-p, --parameters @JSON_FILE | JSON_STRING ] [-g RESOURCE_GROUP] [--service-endpoints SERVICE_ENDPOINTS_TYPE] [--allow-cleanup] [--lock]
   ```
   {: codeblock}

   To list services, use the [`ibmcloud catalog service marketplace`](/docs/cli/reference/ibmcloud?topic=cli-ibmcloud_catalog#ibmcloud_catalog_service_marketplace) command. 
   {: note}

For example, the following command creates a service instance that is named `my-service-instance`, uses service plan `test-   service-plan` of service `test-service` on location `eu-gb`:

   ```bash
   ibmcloud resource service-instance-create my-service-instance test-service test-service-plan eu-gb
   ```
   {: codeblock}

## Creating new resource instances by using the API
{: #create-resource-instance-api} 
{: api}

You can programmatically create a new resource instance by calling the Resource Controller API as shown in the following sample request. For more information, see [Resource Controller API](https://cloud.ibm.com/apidocs/resource-controller/resource-controller#create-resource-instance){: external}.

```bash
curl -X POST \
  https://resource-controller.cloud.ibm.com/v2/resource_instances \
  -H 'Authorization: Bearer <>' \
  -H 'Content-Type: application/json' \
    -d '{
    "name": "my-instance",
    "target": "bluemix-global",
    "resource_group": "5g9f447903254bb58972a2f3f5a4c711",
    "resource_plan_id": "0be5ad401ae913d8ff665d92680664ed",
    "tags": [
      "my-tag"
    ]
  }'
```
{: pre}
{: curl}

```java
CreateResourceInstanceOptions createResourceInstanceOptions = new CreateResourceInstanceOptions.Builder()
  .name(resourceInstanceName)
  .target(targetRegion)
  .resourceGroup(resourceGroup)
  .resourcePlanId(resourcePlanId)
  .build();

Response<ResourceInstance> response = service.createResourceInstance(createResourceInstanceOptions).execute();
ResourceInstance resourceInstance = response.getResult();

System.out.printf("createResourceInstance() response:\n%s\n", resourceInstance.toString());
```
{: codeblock}
{: java}

```javascript
const params = {
  name: resourceInstanceName,
  target: targetRegion,
  resourceGroup: resourceGroupGuid,
  resourcePlanId: resourcePlanId,
};

resourceControllerService.createResourceInstance(params)
  .then(res => {
    instanceGuid = res.result.guid;
    console.log('createResourceInstance() response:\n' + JSON.stringify(res.result, null, 2));
  })
  .catch(err => {
    console.warn(err)
  });
```
{: codeblock}
{: javascript}

```python
resource_instance = resource_controller_service.create_resource_instance(
    name=resource_instance_name,
    target=target_region,
    resource_group=resource_group,
    resource_plan_id=resource_plan_id
).get_result()

print('\ncreate_resource_instance() response:\n',
      json.dumps(resource_instance, indent=2))
```
{: codeblock}
{: python}

```go
createResourceInstanceOptions := resourceControllerService.NewCreateResourceInstanceOptions(
  resourceInstanceName,
  targetRegion,
  resourceGroup,
  resourcePlanID,
)

resourceInstance, response, err := resourceControllerService.CreateResourceInstance(createResourceInstanceOptions)
if err != nil {
  panic(err)
}

b, _ := json.MarshalIndent(resourceInstance, "", "  ")
fmt.Printf("\nCreateResourceInstance() response:\n%s\n", string(b))
```
{: codeblock}
{: go}

## Creating new resource instances by using Terraform
{: #create-resource-instance-terraform}
{: terraform}

You can create new resource instances by using Terraform. 

1. To install the Terraform CLI and configure the {{site.data.keyword.cloud_notm}} Provider plug-in for Terraform, follow the tutorial for [Getting started with Terraform on {{site.data.keyword.cloud}}](/docs/ibm-cloud-provider-for-terraform?topic=ibm-cloud-provider-for-terraform-getting-started). The plug-in abstracts the {{site.data.keyword.cloud_notm}} APIs that are used to complete this task.

2. Create a Terraform configuration file that is named `main.tf`. In this file, you add the configuration to create new resource instances by using HashiCorp Configuration Language. For more information, see the [Terraform documentation](https://www.terraform.io/docs/language/index.html){: external}.

   The following example creates a new resource instance by using the `ibm_resource_instance` resource, where `name` is a unique, descriptive name to identify the resource instance.  
  
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

   You can specify `tags` associated with the resource instance. For more information, see the argument reference details on the [Terraform Resource Management](https://registry.terraform.io/providers/IBM-Cloud/ibm/latest/docs/resources/resource_instance){: external} page.
  
3. Initialize the Terraform CLI.

   ```terraform
   terraform init
   ```
   {: pre}
   
4. Create a Terraform execution plan. The Terraform execution plan summarizes all the actions that need to be run to create a resource instance.

   ```terraform
   terraform plan
   ```
   {: pre}

5. Create the resource instance.

   ```terraform
   terraform apply
   ```

