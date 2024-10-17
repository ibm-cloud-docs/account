---

copyright:
   years: 2021, 2024
lastupdated: "2024-09-10"

keywords: tagging resources, managing access, access management tags, create access management tags, get started with access management tags, IAM-enabled resources, tag your resource, access group, access group policy

subcollection: account

content-type: tutorial
completion-time: 20m

---

{{site.data.keyword.attribute-definition-list}}

# Controlling access to resources by using tags
{: #access-tags-tutorial}
{: toc-content-type="tutorial"}
{: toc-completion-time="20m"}

This tutorial guides you through the steps to centrally manage access to the resources in your account at scale. By completing this tutorial, you learn how to create an access management tag, add the tag to selected resources, set up access groups, invite users, and define a policy to assign access to resources based on the tags on those resources.
{: shortdesc}

Access management tags are metadata that are added to resources to help organize access control relationships. They create flexible and easy to administer resource groupings. When you use tags to control access to your resources, your team's projects can grow without requiring updates to IAM policies.

Let's assume you are the lead of a project for your team that needs an {{site.data.keyword.cos_full}} instance for storing sensitive, project-specific data for analytics. You only want the members of this project to have access to the service instance and work with the project data.

This tutorial applies to IAM-enabled resources only. You need to have an administrator role on the tagging service to create and delete access management tags. To attach and detach access management tags, you need at least an administrator role on the resources to which the tag is added.
{: note}

## Before you begin
{: #access-tag-prereqs}

If you are new to using IAM, check out the following resources to learn more about the features, concepts, and components of the access management system:

* See [What is {{site.data.keyword.Bluemix_notm}} Identity and Access Management?](/docs/account?topic=account-iamoverview) for an overview of the service.
* See [IAM access](/docs/account?topic=account-userroles) for a description of how access management works by using access policies.
* Watch the video about [controlling access by using tags in {{site.data.keyword.cloud_notm}}](/docs/account?topic=account-account_setup#two-teams-projects) for an overview of how to use access management tags.

## Create an access management tag
{: #tagging-resources-create}
{: step}

Create an access management tag that you will attach to your {{site.data.keyword.cos_short}}.

1. Go to **Manage** > **Account** in the {{site.data.keyword.cloud_notm}} console, and select **Tags**.
1. Click **Access management tags**.
1. Enter the name of your tag `project:analysis`, and click **Create tags**. See [Tagging rules](/docs/account?topic=account-tag#limits) for syntax and limitations.

Because tags are visible account-wide, avoid using personal information, such as your name, address, phone number, email address, or other identifying or proprietary information.
{: note}

To learn how you can perform the same actions by using CLI and API commands, see [Working with tags](/docs/account?topic=account-tag).

## Attach your access management tag to a resource
{: #tagging-resources-add}
{: step}

Now that you created your tag, you can add it to your resource.

1. Click the **Navigation Menu** icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Resource List** to access the list of resources in your account.
1. Find your {{site.data.keyword.cos_full}} instance and click the **Actions** icon ![Actions icon](../icons/action-menu-icon.svg "Actions") > **Add tags**.
1. Type `project:analysis` and press Enter.

## Create an access group
{: #tagging-create-access-group}
{: step}

To streamline the process of assigning access to users in your account, you can create an access group. Access groups are a way to organize users and service IDs so that you can easily assign access by adding one or more policies for the entire group.

You'll define the level of access that users have to your {{site.data.keyword.cos_short}} based on the tags that you previously created. See the following examples for each access level:

* With reader role, users can list and download objects in buckets.
* With writer role, users can create and delete buckets.
* With manager role, users can control all aspects of data storage, like adding a retention policy and bucket firewall.

First, create an access group to streamline the task of assigning access to multiple users:

1. In the {{site.data.keyword.cloud_notm}} console, click **Manage** > **Access (IAM)**, and select **Access Groups**.
1. Click **Create**.
1. Enter a unique name to identify your access group, an optional description.
1. Click **Create**.

## Add users to your access group
{: #tagging-add-users-access-group}
{: step}

Then, add users to your access group:

1. Click **Users** > **Add users**.
1. Select the users that you want to add from the list, and click **Add to group**.
1. To add service IDs to the group, click **Service IDs**.
1. Select the IDs that you want to add from the list, and click **Add to group**.

After you create the access policy, access to other resources can be granted or revoked by attaching and detaching the same access management tag to those resources.
{: note}

## Assign a policy
{: #tagging-assign-policy}
{: step}

After you create your access groups, you can assign access to all members of the group with one or more policies. By assigning a group of users access to a group of resources with a single policy, you reduce the overall number of policies that you need to manage.

1. Click **Access** > **Assign access**.
1. Select **All Identity and Access enabled services** as the service.
1. Scope the access to **Specific resources** > **Access management tags** to grant access based on the attached access management tag.
1. Type `project:analysis` or select it from the list of options.
1. Select the resource group access.
1. Select all roles that apply. To view a list of all actions that are mapped to a specific role, click the numbers listed next to each role.
1. Click **Review**.
1. Click **Add** to add your policy configuration to your policy summary.
1. Click **Assign**.

## Invite users
{: #invite-user}
{: step}

You can invite one or multiple users in a single invite. If you invite multiple users in one invitation, the same access is assigned to each user. However, you can invite users to your account with no access, and assign them access later.

1. In the {{site.data.keyword.cloud_notm}} console, go to **Manage** > **Access (IAM)**, and select **Users**.
1. Click **Invite users**. Specify the email addresses of the users. If you are inviting more than one user with a single invitation, they are all assigned the same access.
1. Add one or more of the access options that you manage. You must assign at least one access option. For any access options that you don't add and configure, the default value of **No access** is assigned. Depending on the options that you are authorized to manage, you can assign the following types of access:

* Access groups: Click **Add** for each access group that you want the users to belong to.
   * Access policy: Assign individual IAM access policies or classic infrastructure permissions.
     * Select **Classic infrastructure**, and then select from the three permission sets.
     * Select a group of services like **All Identity and Access enabled services**. Next, you can scope the access to the entire account or just one resource group. Then, select all roles that apply. To view what actions are mapped to each role, click the numbers listed next to each role.

         Some services support the use of advanced operators to grant access to resources that satisfy specific naming conventions. See [Assigning access by using wildcard policies](/docs/account?topic=account-wildcard) for more information.

1. Then, select all roles that apply.
1. Select **Add** to save the access assignment to the invitation.
1. After you add all the necessary access assignments, click **Invite**.

## Manage access for existing users
{: #user_access_manage}
{: step}

After you invite users, you might want to assign more access or edit the existing access to ensure that all members of your account have the correct level of access.

### Assigning new access
{: #new_access}

To assign a new access policy, complete the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, click **Manage** > **Access (IAM)**, and select **Users**.
1. From the row for the user that you want to assign access, click the **Actions** icon ![Actions icon](../icons/action-menu-icon.svg "Actions") > **Assign access**.
1. Select a service or group of services. Then, click **Next**.
1. Scope the access to all resources or specific resources based on selected attributes. Then, click **Next**.
1. Select any combination of roles or permissions to define the scope of access, and click **Review**. For more information, see [IAM roles](/docs/account?topic=account-userroles#iamusermanrol).
1. Click **Add** to add your policy configuration to your policy summary.
1. Click **Assign** to assign all added access to the selected user.

Assign the viewer role or higher to the resource group that contains the resource to ensure that the user can access the resource from their list of resources.
{: tip}

### Editing existing access
{: #editing_access}

You can update existing access by editing the assigned roles for a user.

1. In the {{site.data.keyword.cloud_notm}} console, click **Manage** > **Access (IAM)**, and select **Users**.
1. Select the name of the user that you want to edit access for.
1. Click **Access**.
1. Click the **Actions** icon ![Actions icon](../icons/action-menu-icon.svg "Actions") > **Edit** on the row for the policy that you want to edit.
1. Edit the policy by updating the assigned roles.
1. Click **Save**.

## Next steps
{: #iam-user-next}

Continue securing your cloud resources by creating context-based restrictions, which work with traditional IAM policies, to provide another layer of protection. Or, learn what else you can do with {{site.data.keyword.Bluemix_notm}} IAM by checking out the [features list](/docs/account?topic=account-iamoverview#features).
