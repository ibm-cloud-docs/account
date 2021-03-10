---



copyright:

  years: 2017, 2021
lastupdated: "2021-03-10"

keywords: resource group, account resources, users access to resource groups, create resource group

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:ui: .ph data-hd-interface='ui'}
{:cli: .ph data-hd-interface='cli'}
{:api: .ph data-hd-interface='api'}

# Managing resource groups
{: #rgs}

A resource group is a way for you to organize your account resources in customizable groupings so that you can quickly assign users access to more than one resource at a time. Any account resource that is managed by using {{site.data.keyword.Bluemix}} Identity and Access Management (IAM) access control belongs to a resource group within your account. Cloud Foundry services are assigned to orgs and spaces and can't be added to a resource group.

To start managing your resource groups, in the {{site.data.keyword.cloud}} console, go to **Manage** > **Account** > **Account resources** > **Resource groups**. You can create, view, and rename your resource groups, add resources and manage access to your resource groups. You can also delete any resource group only if it doesn't contain any resources, and it isn't the default resource group. For more information about working with resource groups, see [Best practices for organizing resources and assigning access](/docs/account?topic=account-account_setup).


## Creating a resource group
{: #create_rgs}
{: ui}

If you have a Pay-As-You-Go or Subscription account, you can create multiple resource groups to easily manage quota and view billing usage for a set of resources. You can also group resources to make it easier for you to assign users access to more than one instance at a time.  

You must be assigned an IAM policy with the Administrator role on All Account Management services to create additional resource groups. If you have a Lite account or 30-day trial, you can't create extra resource groups, but you can rename your default resource group.

Connections between a resource group and a Cloud Foundry org or space are restricted by your quota. See [What is an alias?](/docs/account?topic=account-connect_app#what_is_alias) for more information.
{: note}

1. In the console, go to **Manage** > **Account** > **Account resources** > **Resource groups**.
2. Click **Create**.
3. Enter a name for your resource group. 
4. Click **Add**.

### Creating a resource group by using the CLI
{: #rgs_cli}
{: cli}

Run the [`ibmcloud resource group-create`](/docs/cli?topic=cli-ibmcloud_commands_resource#ibmcloud_resource_group_create) command to create a new resource group. For example, the following command creates a resource group that is named `group2`:

```
ibmcloud resource group-create group2
```
{:codeblock}

### Adding resources to a resource group
{: #add_to_rgs}

Services that are managed with IAM belong to a resource group instead of a Cloud Foundry org or space. When you create an instance of one of these services from the catalog, you're prompted to assign the instance to a resource group. Your resource group selection at the time of creating the instance is final and can't be changed.

Users in your account must be assigned two access policies to create resources from the catalog and add them to a resource group:

* A policy with viewer role or higher on the resources group itself
* A policy with editor role or higher on the service in the account

## Renaming a resource group
{: #rename_rgs}
{: ui}

Your first resource group is created and named `Default` for you. You can update the name of this group or any other groups that you create.

1. In the console, go to **Manage** > **Account** > **Account resources** > **Resource groups**.
2. Click the **Actions** ![List of actions icon](../icons/action-menu-icon.svg) menu, and select **Rename**.
3. Enter a unique name and click **Save**.

## Renaming a resource group by using the CLI
{: #renaming-rgs-cli}
{: cli}

Run the [`ibmcloud resource group-update`](/docs/cli?topic=cli-ibmcloud_commands_resource#ibmcloud_resource_group_update) command to update the name of a resource group. For example, the following command renames the `Default` resource group to `Admin`:

```
ibmcloud resource group-update Default [-n, --name Admin]
```
{:codeblock}

## Viewing resources in a resource group
{: #view_rg_resources}
{: ui}

To easily view the resources that are assigned to a resource group, go to the **Menu** icon ![Menu icon](../icons/icon_hamburger.svg) > **My resources**. Then, filter by resource group from the My resources page. 

## Viewing resources by using the CLI
{: #viewing-rgs-cli}
{: cli}

Run the [`ibmcloud resource service-instances`](/docs/cli?topic=cli-ibmcloud_commands_resource#ibmcloud_resource_service_instances) to view the resources that are assigned to a specific resource group. For example, the following command lists all the resources that are in the `Default` resource group:

```
ibmcloud resource service-instances -g Default
```
{:codeblock}





