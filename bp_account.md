---

copyright:

  years: 2018
lastupdated: "2018-10-31"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}

# Best practices for setting up your account
{: #account_setup}

Best practices provide the basic building blocks for success before you start creating resources. If you're ready to get apps to production and set up an environment for your developers, review the following sections to set up your account.
{:shortdesc}

The following best practices focus on using IAM-enabled services. Currently, not all services in {{site.data.keyword.cloud}} are IAM-enabled. If a service instance in your account belongs to a Cloud Foundry org and space, IAM policies, resource groups, and access groups don't apply to it. You can still use both Cloud Foundry orgs and spaces and resource groups in your account, but you must assign users access to those resources separately. For information about working with Cloud Foundry orgs and spaces, see [Adding orgs and spaces](/docs/account/orgs_spaces.html#orgsspacesusers).
{: tip}

## What is a good resource group strategy?
{: #resource-group-strategy}

Since a resource group is a logical container for resources, using one resource group per project environment is a good starting point. This strategy enables administrators to control and see resource usage at the project environment level. For example, a typical project has development, test and production environments. Therefore, a project that is named `CustApp` would have the following resource groups:

* CustApp-Dev
* CustApp-Test
* CustApp-Prod

Access can then be granted to users. For example, a developer typically has fairly wide-ranging access rights to the development resource group and much tighter or no access to the production resource group.

If you have a Pay-As-You-Go or Subscription account, you can create additional resource groups: 

1. Go to **Manage** &gt; **Account** &gt; **Resource groups**.
2. Click **Create a resource group**.
3. Enter the name of your resource group.
4. Click **Add**.

## Setting up your resource groups
{: #setting-up-rgs}

Resource groups are a logical container for organizing your IAM-enabled resources. All services that are managed by using IAM access control belong to a resource group. You assign a resource to its resource group when you create it from the catalog. You can't change the resource group assignment after you set it, which is why it's important to set up some of your resource groups now.

If you have a trial or Lite account, you use the default resource group and can't create any additional ones.
{: tip}

## Adding resources to a resource group
{: #adding-resources}

When you create an IAM-enabled resource from the catalog, the resource group that you want to assign it to must be selected. After a resource is created, you can't change the resource group that it's assigned to. If a mistake is made at this stage, you are required to delete the resource and create a new one.

### Required access for adding a resource to a resource group
{: #rg_access}

The {{site.data.keyword.cloud_notm}} account owner can add resources to any resource group. However, other users must be granted access by using an IAM access policy. There are two minimum platform management roles that users must be assigned to add resources to a resource group:

* Viewer role or higher on the resource group itself
* Editor role or higher on the resource or service

To add a resource to a resource group, complete the following steps:

1. Go to **Manage** &gt; **Account** &gt; **Resource groups**.
2. Click the More Actions icon  ![More Actions icon](../icons/overflow-menu.svg) menu for the resource group that you want to add resources to, and select **Add resources**.
3. When you're redirected to the catalog, select the resource you would like to add.
4. Select the resource group that you want to assign it to.
5. Click **Create**.

You can always go directly to the catalog to create resources and assign them to a resource group.
{: tip} 

For more information, see [Best practices for organizing resources in a resource group](/docs/resources/bestpractice_rgs.html#bp_resourcegroups).

## Next steps

Set up access groups for the users and service IDs that require the same access to resources and resource groups in your account. You can assign a minimal number of access policies, which saves you time. For more information, see [Best practices for assigning access](/docs/iam/bp_access.html).

See [Best practices for organizing users, teams, and applications](/docs/tutorials/users-teams-applications.html#best-practices-for-organizing-users-teams-applications), for more information about setting up users and teams in your account.
