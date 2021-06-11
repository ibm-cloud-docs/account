---

copyright:
  years: 2020, 2021
lastupdated: "2021-06-11"

keywords: user session, end user session, terminate user login, manage account logins, revoke login

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:external: target="_blank" .external}

# Monitoring login sessions
{: #end-user-sessions}

You can review, manage, and revoke your user's active login sessions. You might want to end a session if a login-related credential, such as a refresh token or an IAM cookie is compromised. You can end the active login session that's associated with that credential.
{: shortdesc}

If you are the account owner or assigned the administrator role for the IAM Identity service, you can update the login session settings for all user sessions in the account. For more information about configuring the settings, see [Managing user login sessions](/docs/account?topic=account-iam-work-sessions).

You can review and end your own user sessions from your Profile page. In the {{site.data.keyword.cloud_notm}} console, go to the **{{site.data.keyword.avatar}}** icon ![Avatar icon](../icons/i-avatar-icon.svg "Avatar") > **Profile** > **Sessions**.
{: tip}

## Reviewing user login sessions
{: #review-sessions}

To review current login sessions, complete the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, click **Manage** > **Access (IAM)**, and select **Users**.
1. Select a name from the list.
1. Click **View sessions** in the User details section.

## Ending user login sessions
{: #end-sessions}

When you end an active session, it logs out the user and requires credentials to be entered again. Complete the following steps to end a login session:

1. In the {{site.data.keyword.cloud_notm}} console, click **Manage** &gt; **Access (IAM)**, and select **Users**.
1. Select a name from the list.
1. Click **View sessions** in the User details section.
1. Identify the row with the session details that you want to end.
1. Select the **Actions** icon ![Actions icon](../icons/action-menu-icon.svg "Actions") > **End session**. 
1. Confirm that you want to end the session.
