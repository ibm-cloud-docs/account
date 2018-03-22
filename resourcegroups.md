---



copyright:

  years: 2017, 2018
lastupdated: "2018-03-22"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# Managing resource groups
{: #rgs}

A resource group is a way for you to organize your account resources in customizable groupings, so that you can quickly assign users access to more than one resource at a time. Any account resource that is managed using {{site.data.keyword.Bluemix}} Identity and Access Management (IAM) access control belongs to a resource group within your account. Cloud Foundry services remain assigned to orgs and spaces and cannot be added to a resource group.

To start managing your resource groups, go to **Manage** &gt; **Account** &gt; **Resource Groups** in the {{site.data.keyword.Bluemix}} console. From there you can view your resource groups, rename them, and create new resource groups.


## Creating a resource group

If you have a Pay-As-You-Go or Subscription account, you can create multiple resource groups to easily manage quota and view billing usage for a set of resources. You can also group resources to make it easier for you to assign users access to more than one instance at a time.

If you have a Lite account or 30-day trial, you can't create additional resource groups, but you can rename your default resource group. 

Each resource group is free, however connections between a resource group and a Cloud Foundry org or space count toward your account quota. For more information, see [What is an alias?](/docs/cfapps/connecting_apps.html#what_is_alias).
{: tip}

1. Go to **Manage** &gt; **Account** &gt; **Resource Groups**.
2. Click **Create a resource group**.
3. Enter a name for your resource group.
4. Click **Add**.

## Adding resources to a resource group

Services that are managed using IAM belong to a resource group instead of Cloud Foundry org or space. When you create a service instance for one of these services from the catalog, you are prompted to assign the instance to a resource group. Your resource group selection at the time of creating the instance is final and can't be changed.

## Viewing resources within resource groups

To easily view the resources contained within a resource group, filter by resource group from your dashboard.

## Renaming a resource group

Your first resource group is created and named `Default` for you. You can choose to update the name of this group or any other groups that you create.

1. Go to **Manage** &gt; **Account** &gt; **Resource Groups**.
2. Click **Rename**.
3. Enter a unique name and click **Save**.

## Managing resource groups and resources by using the {{site.data.keyword.Bluemix_notm}} CLI

The {{site.data.keyword.Bluemix_notm}} CLI has mulitple commands that support resource management. For more information, see [Commands for managing resource groups and resources](/docs/cli/reference/bluemix_cli/bx_cli.html#commands-for-managing-resource-groups-and-resources).

## Managing access to your resource groups

Cloud IAM gives you the flexibility to provide fine-grained user access to resources in your account. You can use Cloud IAM to assign policies to users, which provide user access to all resources in a resource group, a single service type within a resource group, or an individual service instance in the account. Providing users access to resources within a resource group does not give them access to manage the resource group itself. You can set access for the ability to view, edit, and manage the actual resource group separately.

For more information on managing access to resource groups, see [Managing IAM access](/docs/iam/mngiam.html#iammanidaccser).
