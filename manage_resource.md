---



copyright:

  years: 2019, 2020
lastupdated: "2020-02-12"

keywords: resource, account resources, create resource, access to create resources

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:term: .term}

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

Use the following steps to create a resource in the console: 
1. From your dashboard, click **View resources** within the Resources summary widget.
2. Click **Create resource**. From here, you are directed to the catalog. You can search the offerings or filter based on a specific category, provider, pricing plan, type of compliance, or release type. Examples of resources include apps, service instances, container clusters, storage volumes, virtual servers, and software. 

After you create the resource, it is displayed in your list of resources on the My resources page.

## Creating resources by using the CLI
{: #create-resource-cli}

To create a resource by using the CLI, run the following command:

```
ibmcloud resource service-instance-create NAME (SERVICE_NAME | SERVICE_ID) SERVICE_PLAN_NAME LOCATION [-d, --deployment DEPLOYMENT_NAME] [-p, --parameters @JSON_FILE | JSON_STRING ] [-g RESOURCE_GROUP] [--service-endpoints SERVICE_ENDPOINTS_TYPE]
```
{: codeblock}

Enter the following command options:
  * **Name (required)**: The name of the service instance. 
  * **SERVICE_NAME or SERVICE_ID (required)**: The name or ID of the service. To list service offerings, use the [`ibmcloud catalog service-marketplace` command](/docs/cli?topic=cli-ibmcloud_catalog#ibmcloud_catalog_service_marketplace).
  * **SERVICE_PLAN_NAME or SERVICE_PLAN_ID (required)**: The name or ID of the service plan.
  * **LOCATION (required)**: The target location or environment to create the service instance.
  * **-d, --deployment DEPLOYMENT_NAME**: The name of the deployment. 
  * **-p, --parameters @JSONFILE or JSON_STRING**: The JSON file or JSON string of parameters to create service instance.
  * **-g RESOURCE_GROUP**: The resource group name. 
  * **--service-endpoints SERVICE_ENDPOINTS_TYPE**: The types of the service endpoints. The possible values are `public`, `private`, `public-and-private`.

The following example shows how to create a resource that is named `my-service-instance` that uses service plan `test-service-plan` of service `test-service` in the `eu-gb` location:

```
ibmcloud resource service-instance-create my-service-instance test-service test-service-plan eu-gb
```

