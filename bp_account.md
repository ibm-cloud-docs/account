---

copyright:
  years: 2018, 2020
lastupdated: "2020-09-21"

keywords: organizing resources, organizing resource groups, account best practices, best practices account, access best practice, my resources 

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}


# Best practices for organizing resources and assigning access
{: #account_setup}

After you set up your {{site.data.keyword.cloud}} account, you're ready to start planning how you want to organize resources and assign access to identities in your account. These best practices provide you with the basic building blocks to enable successful and secure app development in {{site.data.keyword.cloud_notm}}. 
{:shortdesc}

The following best practices focus on resources that are enabled for {{site.data.keyword.cloud_notm}} Identity and Access Management (IAM) and that are assigned to resource groups. Cloud Foundry and classic infrastructure services aren't IAM-enabled, which means that they can't be assigned to resource groups.  
{: note}

## What makes a good resource group strategy?
{: #resource-group-strategy}

Use resource groups to organize your account [resources](#x2004267){: term} for access control and billing purposes. If you're familiar with using Cloud Foundry spaces, think of organizing resources in resource groups similar to the way you organize resources in spaces. 

Administrators can have better control of resource usage at the project environment level if one resource group per project environment is used. For example, a typical project has development, test, and production environments. A project that is named `CustApp` might have the following resource groups:

* CustApp-Dev
* CustApp-Test
* CustApp-Prod

In this scenario, you might assign a developer fairly wide-ranging access to the development resource group and much tighter or no access to the production resource group.

### Organizing resources in resource groups
{: #setting-up-rgs}

All resources that are managed by using IAM access control belong to a resource group. You assign a resource to its resource group when you create it from the catalog. It's important to [create your resource groups](/docs/account?topic=account-rgs#create_rgs) first because you can't change the assignment of resources after you set it. If you accidentally assign a resource to the wrong resource group, delete the resource and create a new one.

A default resource group is created for you when you create a Lite account, and you're limited to the use of one resource group. If you want to create multiple resource groups, [upgrade](/docs/account?topic=account-upgrading-account) to a Pay-As-You-Go or Subscription account. 
{: tip}

### Using tags to organize resources
{: #tags}

A tag is a label that you assign to a resource for easy filtering of resources in your resource list. You can use tags to organize your resources and easily find them later. You can also use tags to help you with identifying specific team usage or cost allocation when you view your [exported usage report](/docs/billing-usage?topic=billing-usage-viewingusage#export-csv).

For more information about tagging resources, see [Working with tags](/docs/account?topic=account-tag).

## How IAM access works
{: #how_access}

After you set up and organize resource groups in your account, you can take advantage of access groups to streamline the access management process. By using access groups, you can minimally manage the number of assigned policies by giving the same access to all identities in an access group.

A policy consists of a subject, target, and role. The subject in this case is the access group. The target is what you want the subject to access, such as a set of resources in a resource group, a service instance, all services in the account, or all instances of a service. The role defines the level of access that is granted.

The most commonly used roles are viewer, editor, operator, and administrator platform roles. 

* The viewer role provides the least amount of access for viewing instances and resource groups in an account. 
* The operator role includes actions such as the ability to view instances and manage aliases, bindings, and credentials.
* The editor role includes actions the same actions of an operator role but also actions for creating, editing, deleting, and binding service instances. 
* The administrator role includes everything for working with a service instance and assigning access to others for that service or instance that the policy is for. 

While these are the most popular roles for assigning access in the platform, there are a second set of roles to consider called service roles. The actions mapped to these roles are defined by each service. Typically the actions mapped to these roles relate specifically to the ability to work with a service's APIs and UI.

For more information about the roles that can be assigned, see [IAM roles](/docs/account?topic=account-userroles#iamusermanrol).

## Reducing time and effort managing access
{: #limit-policies}

There is a [limit](/docs/account?topic=account-known-issues#iam_limits) on the total number of policies that are allowed in an account. There are a few strategies that you can use to ensure that you don't reach the limit and that can help you to reduce the amount of time that you spend assigning and managing access in your account:

* Use resource groups to organize resources that you want a group of developers in your account to use, for example. Then, if all of those developers are in an access group together, you can use the minimum number of policies instead of assigning policies to each developer for each resource.
* Use access groups to organize users and service IDs that all require the same level of access. This way, you can assign a single policy rather than an individual policy for each user or service ID. This way, you assign or revoke access by adding or removing users from the access group.
* Use the principle of least privilege and assign only the access that is required. This can help you ensure that users in your account are limited to only the actions that you want to allow. It also reduces the time that you might need to spend later deleting or reducing assigned access. 

For more best practices from IBM Garage for Cloud, see [Managing access to resources in {{site.data.keyword.cloud_notm}}](https://cloudnativetoolkit.dev/toolkit-resources/resource-mgmt/){: external}.

## What makes a good access group strategy?
{: #accessgroup_strategy}

An access group is an organization of users and service IDs in a grouping to which the same IAM access can be granted. All identities in a single access group inherit the same access.

A logical way to assign access to your resource groups and the included resources is by [creating one access group](/docs/account?topic=account-groups) per required level of access. Then, you can map each access group to the previously created resource groups. For example, to control access to the `CustApp` project, you might create the following access groups:

* Auditor-Group
* Developer-Group
* Admin-Group

For the Auditor-Group, assign two access policies that grant viewer access to the `CustApp-Test` and the `CustApp-Prod` resources and resource groups. For the Developer-Group, assign two access policies that grant editor access to the `CustApp-Dev` and `CustApp-Test` resources and resource groups. For the Admin-Group, assign three access policies that grant administrator access to all three `CustApp` resource groups and their resources.

You can assign administrator access to everything in an account by creating an access group and assigning two policies to it. To create the first policy, use the **IAM services** option, and select **All Identity and Access enabled services** in **All resource groups** with the Administrator platform role, Manager service role, Administrator resource group access role assigned. To create the second policy, use the **Account Management** option, and select **All Account Management Services** with the administrator role assigned.
{: tip}

### Sample access policies
{: #sample_policies}

Review the following sample access policies to help you determine how you might want to assign access to and access group for resources organized in resource groups.

* A policy that grants the access group a platform administrator role on the {{site.data.keyword.containerlong_notm}} across the entire account. The users in the access group can access all instances of this service and create instances of the service in any resource group that the they have at least a viewer role assigned. Access group members with an administrator role assigned on any resource can also grant access to that resource.
* A policy that grants the access group a platform viewer role on a resource group, but not its member resources. The users in the access group have visibility to the resource group, which is required to create instances of any service in this resource group.
* A policy that grants the access group a platform editor role on all resources in the resource group. The users in the access group can edit or delete that resource.
* A policy that grants the access group a platform administrator role on the entire account (all IAM-enabled services). The users in the access group can perform any platform actions on any resource in the entire account and management actions, such as managing the resource groups in the account.

## Use cases for organizing resources and assigning access
{: #usecase_examples}

Review the following use cases to help you prepare a plan that works for your organization. For each use case, it is recommended to use access groups to provide access to a group of users with a minimal number of access policies. By using access groups, you can simply add or remove users from the access groups to assign or revoke access as needed.

### Multiple users working together on a single project
{: #account-ten-users}

Some of the users in your account need to manage the account and assign other users access. Some users need to create service instances that incur expenses. Other users are application developers who need to use only the service instances from their application components.

I want to grant all users various roles in the account and the default resource group. I don't need to create more resource groups to separate resources or restrict some users from accessing some of the resources. I can grant the users the roles that are appropriate for their needs by creating an access group for each group of users:

* Create an access group and assign users to the group who need to manage the account and give others access. Then, assign a policy with an administrator role on the all IAM-enabled services, account management services, and all resource groups.
* Create an access group and assign users to the group who need to create service instances. Then, assign a policy with an editor role on the default resource group and a policy with the editor role for any service the users need to create.
* Create an access group and assign users to the group who need to use the service instances in a resource group. Then, assign a policy with a writer or reader role on the service instances that exist in the resource group.

### Three teams working on three projects
{: #three-teams-projects}

A few users in my account are administrators. They need to create new resource groups and assign users access to them. I assign these users to an access group with a policy that has the administrator role assigned on all IAM-enabled services.

The remaining users only need access to the resource group that's associated with their project. I use access groups and assign various roles on the resource group and its members that are associated with their project: an editor role on the resource group for those who need to create instances, plus a reader or writer role on the resource group members for those who need to use those instances.

### Multiple resource groups in my account
{: #multi-rgs}

Some of the users in my account are the administrators for a service, `Service A`, across my entire account, and they need access to all instances of that service and to create instances. These users don’t need access to other resources in the account. I create an access group and assign an administrator role on Service A at the account level, plus a viewer role for all resource groups in the account.

### A user requiring access to a specific resource
{: #user-specific-resource}

My account includes a user who needs access to only a specific resource in one service, for example, the ability to write to a bucket, `Bucket A`, in {{site.data.keyword.cos_full_notm}}. This user doesn't need to view the resource groups in my account or access other services or buckets in this instance of {{site.data.keyword.cos_short}}.

I assign the user a writer role on Bucket A in the specific instance of {{site.data.keyword.cos_short}}. I can choose to use the IAM UI or the {{site.data.keyword.cos_short}} UI to assign the role. I use the service-specific UI because I can from a list of resources. The IAM UI doesn't display resources past the service instance level, and I need to manually enter the CRN to assign policy to those resources.

## Next steps
{: #bp-access-next}

Now that you know how to set up your resource groups, organize your resources, and create access groups in your account, you can start [inviting users to your account](/docs/account?topic=account-iamuserinv) and assigning them access to your access groups. 

If you already invited users to your account, you can go to your Users page and start [assigning access](/docs/account?topic=account-assign-access-resources#assign_new_access).

