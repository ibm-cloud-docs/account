---

copyright:
   years: 2020, 2021
lastupdated: "2021-11-22"

keywords: get started with IAM, getting started with Identity and Access Management tutorial, IAM tutorial, IAM quick start, resource group, access group, access policy, inviting users

subcollection: account

content-type: tutorial
completion-time: 10m

---

{:shortdesc: .shortdesc}
{:screen: .screen}  
{:codeblock: .codeblock}  
{:pre: .pre}
{:tip: .tip}
{:note: .note}
{:external: target="_blank" .external}
{:step: data-tutorial-type='step'}
{:step-next: data-tutorial-type='step-next'}
{:ui: .ph data-hd-interface='ui'}
{:cli: .ph data-hd-interface='cli'}
{:api: .ph data-hd-interface='api'}
{:terraform: .ph data-hd-interface='terraform'}

# Assigning access to resources by using access groups
{: #access-getstarted}
{: toc-content-type="tutorial"} 
{: toc-completion-time="10m"}

Get up and running quickly with {{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM) by setting up access groups for quick access assignments, inviting users to your account, and managing their access.
{: shortdesc}

This tutorial is for IAM-enabled resources. For services that don't support creating IAM policies for managing access, you can use [Cloud Foundry access](/docs/account?topic=account-cfaccess) or [classic infrastructure permissions](/docs/account?topic=account-infrapermission).
{: note}

## Before you begin
{: #iam-before-you-begin}

If you are new to using IAM, check out the following documentation to learn more about the features, concepts, and components of the access management system:

* [What is IBM Cloud Identity and Access Management?](/docs/account?topic=account-iamoverview) provides a quick overview of what IAM is in {{site.data.keyword.Bluemix_notm}}, the available features, and links to available CLI and API docs.
* [IAM access](/docs/account?topic=account-userroles) gives a more in-depth review of how access management works by using access policies.

## Create access groups
{: #create-access-group}
{: step}
{: ui}

To streamline the process of assigning access to users in your account, you can create an access group. Access groups are a way to organize users and service IDs so that you can easily assign access by adding one or more policies for the entire group. Then, you can add or remove users and service IDs as needed instead of assigning individual access to each user.

A unique name is required to differentiate access groups in the account.
{: note}

### Set up your groups 
{: #group_setup}
{: ui}

To create an access group, complete the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, click **Manage** > **Access (IAM)**, and select **Access Groups**.
2. Click **Create**.
3. Enter a unique name to identify your access group and an optional description.
4. Click **Create**.

Next, continue to set up your group by adding users or service IDs:

1. Select the name of the group that you want to update.
2. Click **Add users**.
3. Select the users that you want to add from the list, and click **Add to group**.
4. To add service IDs to the group, click **Service IDs**.
5. Select the IDs that you want to add from the list, and click **Add to group**.

### Assign access to your groups
{: #group_access}
{: ui}

After you create your access groups, you can assign access to all members of the group with one or more policies. By assigning a group of users access to a group of resources with a single policy, you reduce the overall number of policies that you need to manage.

1. From the **Access policies** tab, click **Assign access**. 
2. Select **IAM services** or **Account management**.
3. Select the type of access that you want to assign.

   If you're assigning access to IAM-enabled services, some services support the use of advanced operators to grant access to resources that satisfy specific naming conventions. See [Assigning access by using wildcard policies](/docs/account?topic=account-wildcard) for more information. 
   {: note}
  
4. Click **Add**. Repeat as needed to add more access.
5. Click **Assign** to assign all added access to your access group. 

## Creating access groups by using Terraform
{: #create-access-group-terraform}
{: terraform}

You can create access groups by using Terraform.

1. To install the Terraform CLI and configure the {{site.data.keyword.cloud_notm}} Provider plug-in for Terraform, follow the tutorial for [Getting started with Terraform on {{site.data.keyword.cloud}}](/docs/ibm-cloud-provider-for-terraform?topic=ibm-cloud-provider-for-terraform-getting-started). The plug-in abstracts the {{site.data.keyword.cloud_notm}} APIs that are used to complete this task.

2. Create a Terraform configuration file that is named `main.tf`. In this file, you add the configuration to create access groups by using HashiCorp Configuration Language. For more information, see the [Terraform documentation](https://www.terraform.io/docs/language/index.html){: external}.

   The following example creates an access group by using the `ibm_iam_access_group` resource, where `name` is a unique name to identify the access group. 

   ```terraform
   resource "ibm_iam_access_group" "accgrp" {
    name        = "test"
    description = "New access group"
   }
   ```
   {: codeblock}

   You can also specify the description of the access group on the `description` option. For more information, see the argument reference details on the [Identity and Access Management (IAM)](https://registry.terraform.io/providers/IBM-Cloud/ibm/latest/docs/resources/iam_access_group){: external} page.
  
3. Initialize the Terraform CLI.

   ```bash
   terraform init
   ```
   {: pre}
   
4. Create a Terraform execution plan. The Terraform execution plan summarizes all the actions that need to be run to create the access group.

   ```bash
   terraform plan
   ```
   {: pre}

5. Create the access group.

   ```bash
   terraform apply
   ```

## Invite users 
{: #invite-user}
{: step}
{: ui}

You can invite one or multiple users in a single invite. If you invite multiple users in one invitation, the same access is assigned to each user. However, you can invite users to your account with no access, and assign them access later.

1. In the console, go to **Manage** > **Access (IAM)**, and select **Users**.
2. Click **Invite users**. Specify the email addresses of the users. If you are inviting more than one user with a single invitation, they are all assigned the same access.
3. Add one or more of the access options that you manage. You must assign at least one access option. For any access options that you don't add and configure, the default value of **No access** is assigned. Depending on the options that you are authorized to manage, you can assign the following types of access:

   * Add users to access groups. Click **Add** for each access group that you want the users to belong to. 
   * Manually assign users access. Expand this section to assign individual IAM access policies, Cloud Foundry roles, or classic infrastructure permissions.
     * Select **Cloud Foundry** > an organization > a region to select a specific space, and assign a space role. An organization and space role are both required to add the access assignment to the invite.
     * Select **Classic infrastructure**, and then select from the three permission sets.
     * Select **IAM services**, and then select the option for all services or just a specific service. Next, you can scope the access to the entire account or just one resource group. Then, select all roles that apply. To view what actions are mapped to each role, click the **Actions for role** option to view a list of all actions that are mapped to a specific role. 
     
         Some services support the use of advanced operators to grant access to resources that satisfy specific naming conventions. See [Assigning access by using wildcard policies](/docs/account?topic=account-wildcard) for more information. 
     
         If you select the **Account** scope for the access policy, the user must already have the Viewer role or higher on the resource group or groups that contain the resources you want the user to have access to. Without a role on a resource group, the user can't work with the resource from the Resource list page in the console.
         {: tip}
     
     * Select **Account management**, and then choose from the all account management services option or select a specific service. Then, select all roles that apply.
  
4. Select **Add** to save the access assignment to the invitation.
5. After you add all the necessary access assignments, click **Invite**.

For more information, see [Inviting users to an account](/docs/account?topic=account-iamuserinv).

## Inviting users by using Terraform
{: #invite-user-terraform}
{: terraform}

You can invite users by using Terraform.

1. To install the Terraform CLI and configure the {{site.data.keyword.cloud_notm}} Provider plug-in for Terraform, follow the tutorial for [Getting started with Terraform on {{site.data.keyword.cloud}}](/docs/ibm-cloud-provider-for-terraform?topic=ibm-cloud-provider-for-terraform-getting-started). The plug-in abstracts the {{site.data.keyword.cloud_notm}} APIs that are used to complete this task.

2. Create a Terraform configuration file that is named `main.tf`. In this file, you add the configuration to invite users by using HashiCorp Configuration Language. For more information, see the [Terraform documentation](https://www.terraform.io/docs/language/index.html){: external}.

   The following example invites users by using the `ibm_iam_user_invite` resource. You can specify the list of invited users on the `users` option. You must have the email ID of a user in order to complete the task.

   ```terraform
   resource "ibm_iam_user_invite" "invite_user" {
    users = ["test@in.ibm.com"]
   }
   ```
   {: codeblock}

   For more information, see the argument reference details on the [Identity and Access Management (IAM)](https://registry.terraform.io/providers/IBM-Cloud/ibm/latest/docs/resources/iam_user_invite){: external} page.
  
3. Initialize the Terraform CLI.

   ```bash
   terraform init
   ```
   {: pre}
   
4. Create a Terraform execution plan. The Terraform execution plan summarizes all the actions that need to be run to invite users.

   ```bash
   terraform plan
   ```
   {: pre}

5. Invite the users.

   ```bash
   terraform apply
   ```

## Manage access for existing users
{: #user_access_manage}
{: step}
{: ui}

After you invite users, you might want to assign more access or edit the existing access to ensure that all members of your account have the correct level of access.

### Assigning new access
{: #new_access}
{: ui}

To assign a new access policy, complete the following steps:

1. In the console, click **Manage** > **Access (IAM)**, and select **Users**.
2. From the row for the user that you want to assign access, click the **Actions** icon ![Actions icon](../icons/action-menu-icon.svg "Actions") > **Assign access**.
3. Click **Add** for each access group that you want the users to belong to.
4. (Optional) If you want to assign additional access to Cloud Foundry roles, classic infrastructure permissions, individual IAM services, or account management services, expand the Assign users additional access section.
5. Select any combination of roles or permissions to define the scope of access, and click **Add**. For more information, see [IAM roles](/docs/account?topic=account-userroles#iamusermanrol).
6. Click **Assign** to assign all added access to the selected user. 
    
Assign the viewer role or higher to the resource group that contains the resource to ensure that the user can access the resource from their list of resources.
{: tip}

### Editing existing access
{: #editing_access}
{: ui}

You can update existing access by editing the assigned roles for a user.

1. In the console, click **Manage** > **Access (IAM)**, and select **Users**.
2. Select the name of the user that you want to edit access for.
3. Click **Access policies**.
4. Click the **Actions** icon ![Actions icon](../icons/action-menu-icon.svg "Actions") > **Edit** on the row for the policy that you want to edit.
5. Edit the policy by updating the assigned roles.
6. Click **Save**.

## Managing access for existing users by using Terraform
{: #user_access_manage_terraform}
{: terraform}

After you invite users, you might want to assign more access or edit the existing access to ensure that all members of your account have the correct level of access.

### Assigning new access by using Terraform
{: #new_access_terraform}
{: terraform}

You can assign new access to a user by using Terraform. 

1. To install the Terraform CLI and configure the {{site.data.keyword.cloud_notm}} Provider plug-in for Terraform, follow the tutorial for [Getting started with Terraform on {{site.data.keyword.cloud}}](/docs/ibm-cloud-provider-for-terraform?topic=ibm-cloud-provider-for-terraform-getting-started). The plug-in abstracts the {{site.data.keyword.cloud_notm}} APIs that are used to complete this task.

2. Create a Terraform configuration file that is named `main.tf`. In this file, you add the configuration to assign new access by using HashiCorp Configuration Language. For more information, see the [Terraform documentation](https://www.terraform.io/docs/language/index.html){: external}.

   The following example creates an IAM policy that grants users the IAM `Viewer` platform role by using the `ibm_iam_user_policy` resource. You must have an existing IBM ID or email address of the user in order to complete the task.

   ```terraform
   resource "ibm_iam_user_policy" "policy" {
    ibm_id = "test@in.ibm.com"
    roles  = ["Viewer"]
   }
   ```
   {: codeblock}

   For more information, see the argument reference details on the [Terraform Identity and Access Management (IAM)](https://registry.terraform.io/providers/IBM-Cloud/ibm/latest/docs/resources/iam_user_policy#user-policy-for-all-identity-and-access-enabled-services){: external} page.
  
3. Initialize the Terraform CLI.

   ```bash
   terraform init
   ```
   {: pre}
   
4. Create a Terraform execution plan. The Terraform execution plan summarizes all the actions that need to be run to assign new access.

   ```bash
   terraform plan
   ```
   {: pre}

5. Assign the new access.

   ```bash
   terraform apply
   ```

### Editing existing access by using Terraform
{: #editing_access_terraform}
{: terraform}

You can update existing access by editing the assigned roles for a user by using Terraform. 

1. To install the Terraform CLI and configure the {{site.data.keyword.cloud_notm}} Provider plug-in for Terraform, follow the tutorial for [Getting started with Terraform on {{site.data.keyword.cloud}}](/docs/ibm-cloud-provider-for-terraform?topic=ibm-cloud-provider-for-terraform-getting-started). The plug-in abstracts the {{site.data.keyword.cloud_notm}} APIs that are used to complete this task.

2. Create a Terraform configuration file that is named `main.tf`. In this file, you add the configuration to update an existing access by using HashiCorp Configuration Language. For more information, see the [Terraform documentation](https://www.terraform.io/docs/language/index.html){: external}.

   You can edit the existing access by updating `roles` with a new value in the following example. 
  
   ```terraform
   resource "ibm_iam_user_policy" "policy" {
    ibm_id = "test@in.ibm.com"
    roles  = ["Viewer"]
   }
   ```
   {: codeblock}

   For more information, see the argument reference details on the [Terraform Identity and Access Management (IAM)](https://registry.terraform.io/providers/IBM-Cloud/ibm/latest/docs/resources/iam_user_policy#user-policy-for-all-identity-and-access-enabled-services){: external} page.
  
3. Initialize the Terraform CLI.

   ```bash
   terraform init
   ```
   {: pre}
   
4. Create a Terraform execution plan. The Terraform execution plan summarizes all the actions that need to be run to update an existing access.

   ```bash
   terraform plan
   ```
   {: pre}

5. Update the existing access.

   ```bash
   terraform apply
   ```

## Next steps
{: #iam-user-next}

Continue securing your cloud resources by creating context-based restrictions, which work with traditional IAM policies, to provide an extra layer of protection. Or, learn what else you can do with {{site.data.keyword.Bluemix_notm}} IAM by checking out the [features list](/docs/account?topic=account-iamoverview#features).
