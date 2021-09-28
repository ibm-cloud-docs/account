---

copyright:
  years: 2015, 2021

lastupdated: "2021-09-28"

keywords: resource FAQs, resource frequently asked questions, resource group, resource list, dashboard widget

subcollection: account

content-type: faq

---


{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:external: target="_blank" .external}
{:note: .note}
{:faq: data-hd-content-type='faq'}


# FAQs about managing resources
{: #resources-faq}

FAQs for managing {{site.data.keyword.cloud_notm}} resources might include questions about working with resource groups, migrating Cloud Foundry instances, and access for working with resources.
{: shortdesc}

## What is a resource group?
{: #resource-group}
{: faq}

A resource group is a way for you to organize your account resources in customizable groupings. Any account resource that is managed by using {{site.data.keyword.Bluemix}} Identity and Access Management (IAM) access control belongs to a resource group within your account. You assign resources to a resource group when you create them from the catalog. You can then view usage per resource group in your account, and easily assign users access to all resources in a resource group or just to a single resource in a resource group.

For more information about creating and working with resource groups, see [Managing resource groups](/docs/account?topic=account-rgs).  

## Why should I migrate my Cloud Foundry service instances to a resource group?
{: #instance-migrated}
{: faq}

Migrating your Cloud Foundry services to a resource group means that the services you're using are now available for use with IAM access control and resource groups. You can take advantage of fine-grained access control by using IAM roles. You can also view usage per resource group in your account. 

When you have Cloud Foundry services that can be migrated to a resource group, you receive a notification on the My resources page. For more information about the migration process, see [Migrating Cloud Foundry service instances and apps to a resource group](/docs/account?topic=account-migrate).

## Why can't I add a resource to a resource group?
{: #create-add-resource}
{: faq}

Most likely you're dealing with an access issue. You must have at least the Viewer role on the resource group itself and at least the Editor role on the service in the account. Learn more in [Adding resources to a resource group](/docs/account?topic=account-rgs#add_to_rgs).

For more information about how to check your assigned access, see [Managing access to resources](/docs/account?topic=account-assign-access-resources#assign-access-resources).

If you need additional access in the account, contact the account owner that is listed on the [Users](/iam/users) page. 

## Who can create resource groups?
{: #create-resource}
{: faq}

You can create resource groups only if you're assigned the Administrator role on All Account Management services in the account. For more information, see [Assigning access to account management services](/docs/account?topic=account-account-services). 

Lite accounts can have only the default resource group, so you can't create any additional resource groups even if you have the required access.

## Can I delete a resource group?
{: #delete-resource-group}
{: faq}

Yes, you can delete a resource group only if it doesn't contain any resources, and it's not the default resource group. See [Deleting a resource group](/docs/account?topic=account-delete_rgs) for more information. 

## How do I add users to a resource group?
{: #add-users-resource-group}
{: faq}

Resource groups are a method of organizing resources and are not directly associated with the management of users. For information on creating a resource group, see [Adding resources to a resource group](/docs/account?topic=account-rgs#add_to_rgs). After your resource group is created, an account administrator can grant access to a specific user. Or, an account administrator can create an access group to provide access to a resource group. For information, see [Creating an Access Group](/docs/account?topic=account-groups#create_ag) in the console. After an access group is created, complete the following steps to associate the access group with a resource group:
 
1. Click **Manage** > **Access (IAM)** and click **Access groups**.
2. Choose an access group. 
3. From the **Access policies** tab, click **Assign access**.
4. Click **IAM services**.  
5. Select the type of access that you want to assign.
6. Scope the access to all resources, or select resources based on specific resource groups as attributes. 
7. Select the platform, service and resource group access for the resource group. 
8. Click **Add** and **Assign**.

You can't use access groups with infrastructure service resources or permissions.
{: note} 

## Can I move service instances between resource groups?
{: #instances-between-rgs}
{: faq}

You can't move service instances between resource groups. If you assign a service instance incorrectly, you must delete and recreate the instance to assign it to another resource group.  

## How do I delete a service from my account?
{: #service-removal}
{: faq}

You can delete a service instance by using the following steps:

1. From your dashboard in the {{site.data.keyword.cloud_notm}} console, click **View resources** within the Resources summary widget.
2. Expand the sections to locate the service instance that you want to delete.
3. Select the **Actions** icon ![Actions icon](../icons/action-menu-icon.svg "Actions") > **Delete** for the row.

## Can I view usage per resource group?
{: #view-usage}
{: faq}

Yes, you can. To access your usage dashboard, go to **Manage** > **Billing and usage** in the console. Select **Usage** to view a summary of the usage by resource group for the account. 

## Who can attach tags to a resource?
{: #tag-faq}
{: faq}

Any user assigned the correct access for the specific type of resource can attach tags. When a resource is tagged, it is visible to all users who have read access to the resource. However, to attach or detach a tag on a resource, certain access roles or permissions are required depending on the resource type and the tag type. For example, to attach user tags to any of the resources that are managed by using IAM, you must be assigned the Editor or Administrator role on the resource.

You can attach access management tags to IAM-enabled resources only.
{: note}

For more information about the required access for other resources types, see [Tagging permissions](/docs/account?topic=account-access#tagging-permissions).

## Where can I find my resources in the {{site.data.keyword.Bluemix_notm}} console?
{: #slitems}
{: faq}

To view all of your resources, select from the following options:

* Click the **Menu** icon ![Menu icon](../icons/icon_hamburger.svg "Menu") > **Resource List**.
* Click the **Menu** icon ![Menu icon](../icons/icon_hamburger.svg "Menu") > **Dashboard**, and click any of the links that are listed in the Resource summary widget.
  
To view just your classic infrastructure resources, select from the following options:

* Click the **Menu** icon ![Menu icon](../icons/icon_hamburger.svg "Menu") > **Classic Infrastructure**.
* Click the **Menu** icon ![Menu icon](../icons/icon_hamburger.svg "Menu") > **Dashboard**, and click any of the links that are listed in the Classic infrastructure widget.
