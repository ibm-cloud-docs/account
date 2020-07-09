---

copyright:

  years: 2018, 2020

lastupdated: "2020-06-01"

keywords: user list visibility, users page setting, user view access, limit access to users list, user list access, parent user, update parent

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}

# Controlling user visibility
{: #iam-user-setting}

There are two ways to change how a user sees other users in an account. The first is the user list visibility setting. And, the second is for classic infrastructure users, and it is directly related to the parent user that is listed. The assigned parent user determines which users that specific user can view when the setting for user list visibility is set to restricted.
{: shortdesc}


## Setting user view access
{: #userlistview}

As an {{site.data.keyword.Bluemix}} account owner, you can view all users in your account and define how users can view other users in the account. By using the user list visibility restriction setting, you can control how users see others across the account.

When the setting is off and the unrestricted view option is selected, any user in the account can view other users from the Users page in {{site.data.keyword.Bluemix_notm}} console. When the setting is on and the **Restricted view** option is selected, users can view only specific types of users in the account:

* Users invited by the user
* Users who share a Cloud Foundry org with the user
* Users who are their descendants in the classic infrastructure user hierarchy, meaning the users that they invited or that one of their descendants invited.

By default, the unrestricted view is set for your account. To update this setting, complete the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, click **Manage** &gt; **Access (IAM)**, and select **Settings**.
2. Select **Restricted view** for the **User list visibility restriction** setting.

## Updating a user's parent user
{: #update-parent}

If you have the correct access, you can update the parent for a user. Updating the parent user affects how a user sees other users in the account when the setting for user list visibility is set to restricted. Users see only other users for which they are a parent and any other users who are invited by those descendants of the parent user.

If you have the following access, you can update the parent for another user:

* An IAM policy with Editor or higher role on the User management service.
* You are an ancestor in the classic infrastructure hierarchy for the user and you have the Manage user classic infrastructure permission assigned

To update a user's parent, complete the following steps:

1. In the {{site.data.keyword.Bluemix}} console, click **Manage** &gt; **Access (IAM)**, and select **Users**.  
2. Select a user name from the list.
3. From the User details page, select a new parent user from the **Parent** menu.
4. Click **Apply**.

