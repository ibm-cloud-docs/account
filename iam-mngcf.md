---

copyright:

  years: 2017, 2021

lastupdated: "2021-06-11"

keywords: Cloud Foundry access, assign access, add user to organization, Cloud Foundry roles

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}

# Managing Cloud Foundry access
{: #mngcf}

To manage access to account organizations and spaces, you must be the account owner, organization manager, or space manager.
{:shortdesc}

## Updating Cloud Foundry access
{: #update_cf_access}

1. In the {{site.data.keyword.cloud}} console, click **Manage** > **Access (IAM)**, and select **Users**.
2. Select the name of the user that you want to assign access. 
3. Select **Cloud Foundry access**.
4. From the row for the organization that you want to manage access, select the **Actions** ![List of actions icon](../icons/action-menu-icon.svg) menu and you can click one of three choices:
  * Remove the user from the organization
  * Edit organization role
  * View organization details


## Adding a user to an organization
{: #add_to_org}

If you are the manager of an organization that the user is not yet a member of, you assign the user to that organization.

1. In the console, click **Manage** > **Access (IAM)**, and select **Users**.
2. From the row for the user that you want to assign access, click the **Actions** icon ![Actions icon](../icons/action-menu-icon.svg) > **Assign access**.
3. Select **Assign users additional access**. 
4. Select the **Cloud Foundry** tile. 
5. Select the organization that you want to assign access to. 
6. Assign the user access:
   * Choose an organization to add the user to
   * Assign an organization role
   * Choose a region
   * Choose a space
   * Assign a space role
7. Click **Add**. Repeat as needed to add more access.
8. Click **Assign** to assign all added access to your access group. 

## Reviewing your assigned access
{: #review_my_access}

If you need to review your assigned access in an account that you have been added to, complete the following steps:

1. In the console, click **Manage** > **Access (IAM)**, and select **Users**.
2. Select your name.
3. Click **Cloud Foundry access**.
3. Expand the org row, and review your assigned roles.

If you need additional access, you must contact the organization manager or account owner to update your assigned Cloud Foundry role.
