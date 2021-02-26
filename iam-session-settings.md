---

copyright:

  years: 2021

lastupdated: "2021-02-24"

keywords: user session, inactivity, sign out

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}

# Managing user log in sessions
{: #iam-work-sessions}

As an account owner or user assigned the administrator role for the identity service, you can improve the security of your account by requiring account users to enter their log in credentials at customized intervals. You can select the time that a user's active session can last before they need to enter their credentials again, and you can also choose the duration that a user can be inactive before they are signed out of their session and need to enter their credentials again. 
{:shortdesc}

## Before you begin
{: #work-sessions-access}

If you have any of the following access, you can update this setting for other users in your account:

* Editor or higher role on the User management service
* You are an ancestor in the classic infrastructure hierarchy for the user and you have the Manage users classic infrastructure permission assigned

## Setting duration of active sessions
{: #sessions-active}

An active session is how long a user has been continuously working on their account. How a active session is gauged also depends on the duration of your session inactivity sign out limit. For instance, if you set the inactivity sign out at two hours, then the user would need to interact with the account one time between those two hours. To update your user's active sessions settings, complete the following steps.


1. In the {{site.data.keyword.cloud_notm}} console, click **Manage** &gt; **Access (IAM)**, and select **Settings**.
1. From the Session settings, click the **Edit** icon ![Edit icon](../icons/icon_write.svg) from the Active sessions tile. 
1. Enter the time limit. The longest a session can last is 24 hours. 
1. Click **Save**. 


## Setting the sign out due to inactivity duration
{: #sessions-inactivity}

An inactive session is one where the user hasn't done anything on their account for the duration selected. If the inactivity sign out duration is one hour, then the user will be signed out after an hour if they haven't done anything on their account in that time. To update your user's inactive sign out sessions settings, complete the following steps.

1. In the {{site.data.keyword.cloud_notm}} console, click **Manage** &gt; **Access (IAM)**, and select **Settings**.
1. From the Session settings, click the **Edit** icon ![Edit icon](../icons/icon_write.svg) from the Sign out due to inactivity tile. 
1. Enter the time limit. The longest an inactive session can last is 2 hours. 
1. Click **Save**. 



