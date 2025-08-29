---
copyright:

  years: 2019, 2025
lastupdated: "2025-08-29"

keywords: resource, account resources, create resource, access to create resources, delete resource, delete instance, search, find, search for instance, search for resource

subcollection: account

---
{{site.data.keyword.attribute-definition-list}}

# Managing resources
{: #manage_resource}

A [resource](x2004267){: term} is anything that you can create from the catalog that is managed by and contained within a resource group. You can create and manage resources by going to your [resource list](https://cloud.ibm.com/resources) in the {{site.data.keyword.cloud}} console or by using the command-line interface (CLI).
{: shortdesc}

Services that are managed by using {{site.data.keyword.Bluemix_notm}} [Identity and Access Management (IAM) access control](/docs/account?topic=account-userroles) and belong to a resource group have several benefits. Because resource groups are not scoped by location, you can create apps and services from different locations in the same resource group. You can also use fine-grained access control down to an individual instance within a resource group.

## Required access for creating resources
{: #creating-resources}

For users in your account to be able to create resources from the catalog and assign them to a resource group, they must be assigned two access policies:

* A policy with viewer role or higher on the resources group itself
* A policy with editor role or higher on the service in the account

## Creating resources in the console
{: #create-resource-console}
{: ui}
{: support}
{: help}

Use the following steps to create a resource in the console:

1. From your dashboard, click **View resources** within the Resources summary widget.
2. Click **Create resource**. From here, you are directed to the catalog. You can search the products or filter based on a specific category, provider, pricing plan, type of compliance, or release type. Examples of resources include apps, service instances, container clusters, storage volumes, virtual servers, and software.

After you create the resource, it is displayed in your list of resources on the Resource list page.

## Creating resources by using the CLI
{: #create-resource-cli}
{: cli}

You can create a resource by using the {{site.data.keyword.Bluemix}} Command Line Interface. For detailed information about working with resources, see [Working with resources and resource groups](/docs/cli?topic=cli-ibmcloud_commands_resource).
1. Log in, and select the account.
   ```bash
   ibmcloud login
   ```
   {: codeblock}

2. Create an organization by running the [`ibmcloud resource service-instance-create`](/docs/cli?topic=cli-ibmcloud_commands_resource#ibmcloud_resource_service_instance_create) command.

In this command,`NAME` is the name of the service instance, `SERVICE_NAME or SERVICE_ID` is the name or ID of the service, `SERVICE_PLAN_NAME or SERVICE_PLAN_ID`is the name or ID of the service plan, and `LOCATION`is the target location or environment to create the service instance.

   ```bash
   ibmcloud resource service-instance-create NAME (SERVICE_NAME | SERVICE_ID) SERVICE_PLAN_NAME LOCATION [-d, --deployment DEPLOYMENT_NAME] [-p, --parameters @JSON_FILE | JSON_STRING ] [-g RESOURCE_GROUP] [--service-endpoints SERVICE_ENDPOINTS_TYPE] [--allow-cleanup] [--lock]
   ```
   {: codeblock}

   To list services, use the [`ibmcloud catalog service-marketplace`](/docs/cli?topic=cli-ibmcloud_catalog#ibmcloud_catalog_service_marketplace) command.
   {: note}

For example, the following command creates a service instance that is named `my-service-instance`, uses service plan `test-   service-plan` of service `test-service` on location `eu-gb`:

   ```bash
   ibmcloud resource service-instance-create my-service-instance test-service test-service-plan eu-gb
   ```
   {: codeblock}

## Creating new resource instances by using the API
{: #create-resource-instance-api}
{: api}

You can programmatically create a new resource instance by calling the Resource Controller API as shown in the following sample request. For detailed information about the API, see [Resource Controller API](https://cloud.ibm.com/apidocs/resource-controller/resource-controller#create-resource-instance){: external}.
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


## Installing software by using the API
{: #install-software-api}
{: api}

You can install software only through the console or CLI. To see the steps, switch to the UI or CLI instructions.

## Creating new resource instances by using Terraform
{: #create-resource-instance-terraform}
{: terraform}

Before you can create new resource instances by using Terraform, make sure that you have completed the following:

- Install the Terraform CLI and configure the {{site.data.keyword.cloud_notm}} Provider plug-in for Terraform. For more information, see the tutorial for [Getting started with Terraform on {{site.data.keyword.cloud}}](/docs/ibm-cloud-provider-for-terraform?topic=ibm-cloud-provider-for-terraform-getting-started). The plug-in abstracts the {{site.data.keyword.cloud_notm}} APIs that are used to complete this task.

- Create a Terraform configuration file that is named `main.tf`. In this file, you define resources by using HashiCorp Configuration Language. For more information, see the [Terraform documentation](https://developer.hashicorp.com/terraform/language){: external}.

You can create new resource instances by using Terraform.

1. Create an argument in your `main.tf` file. The following example creates a new resource instance by using the `ibm_resource_instance` resource, where `name` is a unique, descriptive name to identify the resource instance.
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

## Searching for resources
{: #searching-for-resources}

You can search for resources from anywhere in the {{site.data.keyword.cloud}} console. Enter the resource or tag in the search field from the console menu bar. You can also use the {{site.data.keyword.Bluemix_notm}} command-line interface (CLI) to search across your resources. The CLI searches for distributed applications and service instances across locations and data centers. [The Global Search and Tagging - Search API](https://cloud.ibm.com/apidocs/search) supports searching for resources as well.

## Refining your search results
{: #results}
{: ui}

View all catalog results
:   Use this option to view a filtered catalog search. The first five results are displayed by name. If you want a more detailed search criteria for catalog entries, such as searching the description, you can click this link and get a filtered catalog results view. This option helps you find the offerings that you want to create faster. This appears if it matches to a catalog result. This field doesn't appear if your search query starts with `tag:`.

Search support cases
:   Use this option to filter by your open support cases across the platform, including infrastructure resources. This shows up at the end of the search if you search for anything, including if you search by `tag:`.

Search in {{site.data.keyword.cloud_notm}} docs
:   Use this option to get a filtered search of the documentation. This shows up at the end of any search, including if you search by `tag:`.

Press the Forward Slash key (/) to navigate your cursor to the search field.
{: tip}

## Searching with the CLI
{: #searching-cl}
{: cli}

You can also search across all your resources by using Lucene query syntax, with a single command by using the {{site.data.keyword.Bluemix_notm}} CLI.
The most commonly used resource attributes that you can query and retrieve are:

`name`
:   The user-defined name of the resource.

`region`
:   The geographical location where the resource is created. The allowed values are, for example, `us-south`, `us-east`, `au-syd`, `eu-gb`, `eu-de`, and `jp-tok`.

`service_name`
:   The name of the service as it appears in the `service-name` segment of the resource's CRN. You can get the allowed values from the **Name** column of the output of `ibmcloud catalog service-marketplace`.

`resource_group_id`
:   The resource group ID of the resource.

`type`
:   The resource type as it appears in the `resource-type` segment of the resource's CRN if present. Values depend on the owning service. Example values are: `k8-cluster` for `containers-kubernetes` service; `k8-location` and `k8-connector` for `satellite` service; `resource-group` for `resource-controller` service; `vpc`, `volume`, `vpn`, `load-balancer`, `security-group`, for `is` service; `workspace` for `schematics` service.

`creation_date`
:   The date on which the resource is created.

`modification_date`
:   The last modification date of the resource.

`tags`
:   The tags attached to the resource.

`access_tags`
:   The access management tags attached to the resource.

`service_tags`
:   The service tags attached to the resource.

`tagReferences.tag.name`
:   The tags that have been attached to a classic infrastructure resource. Requires you to specify `-p classic-infrastructure` parameter.

`_objectType:`
:   The object type of the classic infrastructure resource. Allowed values are: `SoftLayer_Virtual_DedicatedHost`, `SoftLayer_Hardware`, `SoftLayer_Network_Application_Delivery_Controller`, `SoftLayer_Network_Subnet_IpAddress`, `SoftLayer_Network_Vlan`, `SoftLayer_Network_Vlan_Firewall`, `SoftLayer_Virtual_Guest`. Requires you to specify `-p classic-infrastructure` parameter.

`tagReferences.tag.name` and `_objectType` are only valid when using the `-p classic-infrastructure` flag.
{: note}

The usage of `-p classic-infrastructure` for _objectType `SoftLayer_Virtual_DedicatedHost`, `SoftLayer_Network_Vlan_Firewall`, `SoftLayer_Virtual_Guest` and `SoftLayer_Hardware` (for the classic infrastructure bare metal servers only) is deprecated since now they are searchable as all other not classic infrastructure resources.
{: note}

### Searching for classic infrastructure resources
{: #search-classic-infra-resources}

To search for classic infrastructure resources, the string must be contained within double quotation marks in order for an exact match for the query string to be returned.
In addition, if you enter a search term that includes a hyphen (-) and you don't surround the string with a double quotation mark, the search will not return an exact match. Hyphens within the string are used to break the term into multiple strings.

### Search examples
{: #resource-name}

The following examples can help you search for account resources.
When the `-p classic-infrastucture` parameter is not specified search spans across all resources but classic infrastructure resources with `_objectType` `SoftLayer_Network_Application_Delivery_Controller`, `SoftLayer_Network_Subnet_IpAddress`, or `SoftLayer_Hardware` (excluding bare metal servers).

* To search for all your resources named `ABC`, enter the following command:

    ```bash
    ibmcloud resource search ‘name:ABC’
    ```
    {: codeblock}

* To search for all service instances of Message Hub, enter the following command:

    ```bash
    ibmcloud resource search 'service_name:messagehub'
    ```
    {: codeblock}

* To search for resources that are not classic infrastructure that were created between 16 May 2020 and 20 May 2020, enter the following command:

    ```bash
    ibmcloud resource search 'creation_date:["2020-05-16T00:00:00Z" TO "2020-05-20T00:00:00Z"]'
    ```
    {: codeblock}

* To search for resources that are not classic infrastructure whose name starts with "my", ordered by type, enter the following command:

    ```bash
    ibmcloud resource search 'name:my*' -s type
    ```
    {: codeblock}

* To search for resources that are not classic infrastructure and have been tagged with `my-tag`, enter the following command:

    ```bash
    ibmcloud resource search 'tags:my-tag'
    ```
    {: codeblock}

* To search for all classic infrastructure virtual servers whose fully qualified domain name is `MyVM`, enter the following command:
    ```bash
    ibmcloud resource search “doc.fullyQualifiedDomainName:MyVM AND service_name:virtual-server"
    ```
    {: codeblock}

* To search for all classic infrastructure resources that have been tagged with `my-tag`, enter the following command:

    ```bash
    ibmcloud resource search 'tagReferences.tag.name:my-tag' -p classic-infrastructure
    ```
    {: codeblock}

* To search for all classic infrastructure of type `SoftLayer_Network_Vlan`, enter the following command:

    ```bash
    ibmcloud resource search '_objectType:SoftLayer_Network_Vlan' -p classic-infrastructure
    ```
    {: codeblock}

## Search by using the API
{: #searching-api}
{: api}

To search for resources, call [The Global Search and Tagging - Search API](https://cloud.ibm.com/apidocs/search#search). The following example searches for all resources with tag "project:myproject" attached.

Use the `SearchOptions.Builder` to create a `SearchOptions` object that contains the parameter values for the `search` method.
{: java}

Instantiate the `SearchOptions` struct and set the fields to provide parameter values for the `Search` method.
{: go}

```bash
curl -X POST -H "Authorization: {iam_token}" -H "Accept: application/json" -H "Content-Type: application/json" -d '{"query": "tags:project\\:myproject OR access_tags:project\\:myproject", "fields": ["*"]}' "api.global-search-tagging.cloud.ibm.com/v3/resources/search"
```
{: codeblock}
{: curl}

```java
SearchOptions searchOptions = new SearchOptions.Builder()
  .query("GST-sdk-*")
  .fields(new java.util.ArrayList<String>(java.util.Arrays.asList("*")))
  .searchCursor(searchCursor)
  .build();

Response<ScanResult> response = service.search(searchOptions).execute();
ScanResult scanResult = response.getResult();

System.out.println(scanResult);
```
{: codeblock}
{: java}

```javascript
const params = {
  query: 'GST-sdk-*',
  fields: ['*'],
  searchCursor: searchCursor,
};

globalSearchService.search(params)
  .then(res => {
    console.log(JSON.stringify(res.result, null, 2));
  })
  .catch(err => {
    console.warn(err)
  });
```
{: codeblock}
{: javascript}

```python
response = global_search_service.search(query='GST-sdk-*',
                    fields=['*'])
scan_result = response.get_result()

print(json.dumps(scan_result, indent=2))
```
{: codeblock}
{: python}

```go
searchOptions := globalSearchService.NewSearchOptions()
searchOptions.SetLimit(10)
searchOptions.SetQuery("GST-sdk-*")
searchOptions.SetFields([]string{"*"})

scanResult, response, err := globalSearchService.Search(searchOptions)
if err != nil {
  panic(err)
}
b, _ := json.MarshalIndent(scanResult, "", "  ")
fmt.Println(string(b))
```
{: codeblock}
{: go}

## Deleting resources
{: #delete-resource}

When you don't need a resource in your account anymore, or if a user in your account created a resource that you don't want them to use, you can delete the instance from your account.

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

You can also delete a resource instance by running the following `terraform destroy` command:

```terraform
terraform destroy -target RESOURCE_TYPE.NAME -target RESOURCE_TYPE2.NAME
```
{: pre}
