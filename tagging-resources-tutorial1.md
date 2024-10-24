---

copyright:
   years: 2021, 2024
lastupdated: "2024-10-24"

keywords: tagging resources, managing access, access management tags, create access management tags, get started with access management tags, IAM-enabled resources, tag your resource, access group, access group policy

subcollection: account

content-type: tutorial
completion-time: 10m

---

{{site.data.keyword.attribute-definition-list}}

# Controlling access to resources by using tags
{: #access-tags-tutorial}
{: toc-content-type="tutorial"}
{: toc-completion-time="10m"}

This tutorial guides you through the steps to centrally manage access to the resources in your account at scale. By completing this tutorial, you learn how to create an access management tag, add the tag to selected resources, and define a policy to assign access to resources based on the tags on those resources.
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
2. Click **Access management tags**.
3. Enter the name of your tag `project:analysis`, and click **Create tags**. See [Tagging rules](/docs/account?topic=account-tag#limits) for syntax and limitations.

Because tags are visible account-wide, avoid using personal information, such as your name, address, phone number, email address, or other identifying or proprietary information.
{: note}

## Attach your access management tag to a resource
{: #tagging-resources-add}
{: step}

Now that you created your tag, you can add it to your resource.

1. Click the **Navigation Menu** icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Resource List** to access the list of resources in your account.
2. Find your {{site.data.keyword.cos_full}} instance and click the **Actions** icon ![Actions icon](../icons/action-menu-icon.svg "Actions") > **Add tags**.
3. Type `project:analysis` and press Enter.

## Create an access group
{: #tagging-create-access-group}
{: step}

You'll define the level of access that users have to your {{site.data.keyword.cos_short}} based on the tags that you previously created. See the following examples for each access level:
* With reader role, users can list and download objects in buckets.
* With writer role, users can create and delete buckets.
* With manager role, users can control all aspects of data storage, like adding a retention policy and bucket firewall.

First, create an access group to streamline the task of assigning access to multiple users:

1. Click **Manage** > **Access (IAM)** in the {{site.data.keyword.cloud_notm}} console, and select **Access groups**.
2. Click **Create**.
3. Enter a unique name to identify your access group, an optional description, and click **Create**.

## Assign a policy
{: #tagging-assign-policy}
{: step}

Next, assign a policy to the group:

1. Click **Access** > **Assign access**.
1. Select **All Identity and Access enabled services** as the service.
1. Scope the access to **Specific resources** > **Access management tags** to grant access based on the attached access management tag.
1. Type `project:analysis` or select it from the list of options.
1. Select the resource group access.
1. Select all roles that apply. To view a list of all actions that are mapped to a specific role, click the numbers listed next to each role.
1. Click **Review**.
1. Click **Add** to add your policy configuration to your policy summary.
1. Click **Assign**.

## Add users to your access group
{: #tagging-add-users-access-group}
{: step}

Then, add users to your access group:

1. Click **Users** > **Add users**.
2. Select the members of the project from the list, and click **Add to group**.

After you create the access policy, access to other resources can be granted or revoked by attaching and detaching the same access management tag to those resources.
{: note}

## Next steps
{: #tagging-resources-next}

To learn how you can perform the same actions by using CLI and API commands, see [Working with tags](/docs/account?topic=account-tag).
