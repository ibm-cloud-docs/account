---

copyright:

  years: 2015, 2025
lastupdated: "2025-04-14"

keywords: resource FAQs, resource frequently asked questions, resource group, resource list, dashboard widget, delete service, cancel service, cancel resource

subcollection: account

content-type: faq

---

{{site.data.keyword.attribute-definition-list}}

# FAQ about managing resources
{: #resources-faq}

FAQ about managing resources includes answers to common questions about resource groups in {{site.data.keyword.cloud_notm}}, including how they help organize resources, who can create and manage them, and how access is controlled. You will also learn about tagging, usage tracking, deleting services, and how resource groups integrate with access groups. To find all FAQ for {{site.data.keyword.cloud}}, see our [FAQ library](/docs/faqs).
{: shortdesc}

## What is a resource group?
{: #resource-group}
{: faq}

A resource group is a way for you to organize your account resources in customizable groupings. Any account resource that is managed by using {{site.data.keyword.Bluemix}} Identity and Access Management (IAM) access control belongs to a resource group within your account. You assign resources to a resource group when you create them from the catalog. You can then view usage per resource group in your account, and easily assign users access to all resources in a resource group or just to a single resource in a resource group.

For more information about creating and working with resource groups, see [Managing resource groups](/docs/account?topic=account-rgs).

## Why can't I add a resource to a resource group?
{: #create-add-resource}
{: faq}
{: support}

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

Yes, you can delete a resource group only if it doesn't contain any resources, and it's not the default resource group. See [Deleting a resource group](/docs/account?topic=account-rgs#delete_rgs) for more information.

## How do I add users to a resource group?
{: #add-users-resource-group}
{: faq}

Resource groups are a method of organizing resources and are not directly associated with the management of users. For information on creating a resource group, see [Adding resources to a resource group](/docs/account?topic=account-rgs#add_to_rgs). After your resource group is created, an account administrator can grant access to a specific user. Or, an account administrator can create an access group to provide access to a resource group. For information, see [Creating an Access Group](/docs/account?topic=account-groups#create_ag) in the console. After an access group is created, complete the following steps to associate the access group with a resource group:

1. In the {{site.data.keyword.cloud_notm}} console, click **Manage** > **Access (IAM)** and click **Access groups**.
2. Select an access group.
3. Click **Access** > **Assign access**.
4. Select a service, or group of services.
5. Click **Next**.
6. Scope the access to all resources, or select specific resources and select the resource groups attribute. Then, click **Next**.
7. Select the platform, service and resource group access for the resource group.
8. Click **Review**.
9. Click **Add** to add your policy configuration to your policy summary.
10. Click **Assign**.

You can't use access groups with infrastructure service resources or permissions. {: note}

## Can I move service instances between resource groups?
{: #instances-between-rgs}
{: faq}

You can't move service instances between resource groups. If you assign a service instance incorrectly, you must delete and recreate the instance to assign it to another resource group.

## How do I delete a service from my account?
{: #service-removal}
{: faq}

You can delete a service instance by using the following steps:

1. From the {{site.data.keyword.cloud}} console, click the Navigation Menu icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Resource list** to view your list of resources.
2. Expand the sections to locate the service instance that you want to delete.
3. Click the **Actions** icon ![Actions icon](../icons/action-menu-icon.svg "Actions") > **Delete** for the row.

## Can I view usage per resource group?
{: #view-usage}
{: faq}

Yes, you can. To access your usage dashboard, go to **Manage** > **Billing and usage** in the {{site.data.keyword.cloud_notm}} console. Select **Usage** to view a summary of the usage by resource group for the account.

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

To view all of your resources, click the **Navigation Menu** icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Resource List**.

To view just your classic infrastructure resources, select from the following options:

* Click the **Navigation Menu** icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Classic Infrastructure**.
* Click the **Navigation Menu** icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Dashboard**, and click any of the links that are listed in the Classic infrastructure widget.

## What causes resource restorations to fail?
{: #reclamation-fail}
{: faq}

A resource restoration can fail if you try to restore a resource in a deleted resource group or the resource restoration request isn't submitted in time. Most requests must be submitted within 7 days.

## How do I retrieve details on a resource that is scheduled for reclamation?
{: #reclamation-list}
{: faq}

After the instance is deleted from the console, you can view it in your account by using the CLI in the SCHEDULED state. The SCHEDULED state indicates that this instance is scheduled for reclamation. For more information, see [Working with resources and resource groups](/docs/account?topic=account-ibmcloud_commands_resource#ibmcloud_resource_reclamations).

## Can you restore a resource that is in a deleted resource group?
{: #reclamation-delete}
{: faq}

You can restore a resource from a deleted resource group. [Create a support case](/unifiedsupport/cases/add){: external} in the {{site.data.keyword.Bluemix_notm}} Support Center and specify in the description of the case that you want to restore the resource that's in a deleted resource group.

## How can I share a product or location with my entire enterprise?
{: #visibility-enterprise}
{: faq}

You can share a product, a specific pricing plan within that product, or its deployment with the whole enterprise account or with a specific group within the enterprise. Similarly, you can do the same with any private or public location. If your product or location is managed by using a private catalog, you can [share your product by using the console](/docs/account?topic=account-catalog-share&interface=ui#ent-share-steps). If your product or location is not managed by private catalogs or you aren’t sure, contact your {{site.data.keyword.IBM_notm}} focal to help you get the appropriate information allowlisted into your locations. The same prefixes apply in this scenario and can be done programmatically or in the console. Enterprise IDs are prefixed by `-ent-`, and account groups are prefixed by `-entgrp-`. If you add any new accounts or account groups to the enterprise, they inherit the visibility of that product or location.
