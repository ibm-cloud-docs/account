---

copyright:

  years: 2018
lastupdated: "2018-11-28"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}


# Best practices for setting up your account
{: #account_setup}

These best practices provide you with the basic building blocks for achieving success before you start creating resources. If you're ready to get apps to production and set up an environment for your developers, review the following sections to set up your account.
{:shortdesc}

The following best practices focus on using IAM-enabled services. Currently, not all services in {{site.data.keyword.cloud}} are IAM-enabled. IAM policies, resource groups, and access groups don't apply to service instances that belong to a Cloud Foundry org and space. You can still use both Cloud Foundry orgs and spaces, and resource groups in your account, but you must assign users access to those resources separately. For information about Cloud Foundry orgs and spaces, see [Adding orgs and spaces](/docs/account/orgs_spaces.html#orgsspacesusers).
{: note}

## What makes a good resource group strategy?
{: #resource-group-strategy}

Administrators can have better control of resource usage at the project environment level if one resource group per project environment is used. For example, a typical project has development, test, and production environments. A project that is named `CustApp` would have the following resource groups:

* `CustApp-Dev`
* `CustApp-Test`
* `CustApp-Prod`

You can grant access to users. For example, a developer typically has fairly wide-ranging access permissions to the development resource group and much tighter or no access to the production resource group.

If you have a Pay-As-You-Go or Subscription account, you can create more resource groups: 

1. Go to **Manage** > **Account**, and select **Resource groups** from the **Account resources** menu. 
3. Click **Create**.
4. Enter the name of your resource group.
5. Click **Add**.

For more information about which account type will work best for you, see [Account types](/docs/account/index.html#accounts). 


## Setting up your resource groups
{: #setting-up-rgs}

Resource groups are a logical container for organizing your IAM-enabled resources. All services that are managed by using {{site.data.keyword.cloud_notm}} Identity and Access Management (IAM) access control belong to a resource group. You assign a resource to its resource group when you create it from the catalog. You can't change the resource group assignment after you set it, which is why it's important to set up some of your resource groups now.

If you have a Lite account, you have access to a single resource group that's created for you. You can't create extra resource groups. Consider [upgrading your account](/docs/account/account_settings.html#upgrading-account) to create and work with multiple resource groups. 
{: note}


## Adding resources to a resource group
{: #adding-resources}

You can add a resource to a resource group when you create an IAM-enabled resource from the catalog. When you select the resource, make sure that the target resource group is selected. After a resource is created, you can't change its assigned resource group. If you accidentally assign a resource to the wrong resource group, delete the resource and create a new one.

### Required access for adding a resource to a resource group
{: #rg_access}

As an account owner, you can add resources to any resource group. Other users must be granted access by using an IAM access policy to add resources to resource groups. There are two minimum platform management roles that users must be assigned to add resources to a resource group:

* Viewer role or higher on the resource group
* Editor role or higher on the resource or service

To add a resource to a resource group, complete the following steps:

1. Go to **Manage > Account**, and select **Resource groups**.
2. Click the Actions icon ![Actions icon](../icons/action-menu-icon.svg) for the resource group that you want to add resources to, and select **Add resources**.
3. After you're redirected to the catalog, select the resource you would like to add.
4. Select the resource group that you want to assign it to.
5. Click **Create**.

You can always go directly to the catalog to create resources and assign them to a resource group.
{: tip} 

For more information, see [Best practices for organizing resources in a resource group](/docs/resources/bestpractice_rgs.html#bp_resourcegroups).


## Using tags to organize resources
{: #tags}

Use tags to organize your resources and track usage costs. You can tag related resources and view them throughout your account by filtering by tags from your dashboard. Key:value pair tags can help you organize your development environments, projects, compliance, and optimization. 

To add a tag to a resource, complete the following steps:

1. Click the Menu icon ![Menu icon](../icons/icon_hamburger.svg) > **Resource list** to view your list of resources. Find the resource that you want to tag.
2. If the resource already has a tag, hover over the existing tag and click the Edit icon ![Edit icon](../icons/edit-tagging.svg). If the resource doesn't have a tag, hover over **--** in the `Tags` column, and click **Add tags**. 
3. Type a name for the tag, and press Enter after each tag if you're adding more than one.
4. To remove a tag from the resource, click the Remove icon ![Remove icon](../icons/close-tagging.svg) next to the tag. 
5. Save your changes. 

For more information about what resources can be tagged and how to assign access to delegate tagging functionality to users on your account, see [Working with tags](/docs/resources/tagging_resources.html#tag).


## Next steps

Set up access groups for the users and service IDs that require the same access to resources and resource groups in your account. You can assign a minimal number of access policies, which saves you time. For more information, see [Best practices for assigning access](/docs/iam/bp_access.html).
