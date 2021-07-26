---

copyright:

  years: 2021

lastupdated: "2021-07-26"

keywords: user session, inactivity, sign out, concurrent, login session, trusted profiles

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}

# Setting limits for login sessions
{: #iam-work-sessions}

Improve the security of your account by requiring account users to enter their login credentials at customized intervals. As an account owner or user assigned the administrator role for the Identity service, you can select the time that a user's active session can last before they need to enter their credentials again. You can also choose the duration that a user is inactive before they are signed out of their session and are required to enter their credentials again. 
{:shortdesc}

To review and end active sessions to help maintain the security of your account, see [Monitoring login sessions](/docs/account?topic=account-end-user-sessions).
{: tip}

## Before you begin
{: #work-sessions-access}

If you have the following access, you can update the settings for login sessions:

* Account owners 
* Editor or admin role on all account management services
* Editor or admin role on IAM identity service

A user can have several different restrictions if they are a member of multiple accounts.
{: note}

## Setting duration of active sessions
{: #sessions-active}

An active session is how long a user is continuously working in their account. How an active session is gauged also depends on the duration of your session sign out due to inactivity limit. For instance, if you set the sign out to 2 hours, then the user would need to interact with the account one time between those 2 hours. 

To update your user's active sessions settings, complete the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, click **Manage** > **Access (IAM)**, and select **Settings**.
1. From the Login session section, click the **Edit** icon ![Edit icon](../icons/icon_write.svg "Edit") from the Active sessions tile. 
1. Enter the time limit. The longest a session can last is 720 hours. 
1. Click **Save**. 

### Setting session duration for trusted profiles
{: #sessions-active-tp}

For more information, see [Updating trusted profiles](/docs/account?topic=account-trusted-profile-update#session-limit-tp).

## Setting the sign out due to inactivity duration
{: #sessions-inactivity}

An inactive session is one where the user hasn't completed any requests that send a token for validation for the duration selected. If the sign out due to inactivity duration is 1 hour, then the user will be signed out after an hour if they haven't done anything on their account in that time. To update your user's sign out due to inactivity settings, complete the following steps.

1. In the {{site.data.keyword.cloud_notm}} console, click **Manage** &gt; **Access (IAM)**, and select **Settings**.
1. From the Login session section, click the **Edit** icon ![Edit icon](../icons/icon_write.svg "Edit") from the Sign out due to inactivity tile. 
1. Enter the time limit. The longest an inactive session can last is 24 hours. 
1. Click **Save**. 


## Setting the number of allowed concurrent sessions
{: #sessions-concurrent}

You can choose the maximum number of concurrent sessions that are allowed for your account users. Concurrent sessions are active sessions that the user is signed into at one time. Users can have multiple sessions open by using different browsers or several logins with the {{site.data.keyword.cloud_notm}} CLI. Multiple concurrent sessions are more beneficial for parallel workloads.

1. In the {{site.data.keyword.cloud_notm}} console, click **Manage** > **Access (IAM)**, and select **Settings**.
1. From the Concurrent sessions tile, click the **Edit** icon ![Edit icon](../icons/icon_write.svg "Edit"), click the Unlimited dropdown > **Limit sessions**.
1. Enter the limit. Users can have an unlimited number of concurrent sessions. 
1. Click **Save**. 
