---

copyright:

  years: 2021

lastupdated: "2021-03-22"

keywords: user session, inactivity, sign out, concurrent

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}

# Managing user login sessions
{: #iam-work-sessions}

Improve the security of your account by requiring account users to enter their log in credentials at customized intervals. As an account owner or user assigned the administrator role for the identity service, you can select the time that a user's active session can last before they need to enter their credentials again, and you can also choose the duration that a user can be inactive before they are signed out of their session and need to enter their credentials again. 
{:shortdesc}

## Before you begin
{: #work-sessions-access}

If you have following access, you can update this setting for other users in your account:

* Account owners or users assigned the administrator role for the IAM Identity service
* You are an ancestor in the classic infrastructure hierarchy for the user and you have the Manage users classic infrastructure permission assigned

## Setting duration of active sessions
{: #sessions-active}

An active session is how long a user is continuously working on their account. How an active session is gauged also depends on the duration of your session inactivity sign out limit. For instance, if you set the inactivity sign out at two hours, then the user would need to interact with the account one time between those two hours. To update your user's active sessions settings, complete the following steps.


1. In the {{site.data.keyword.cloud_notm}} console, click **Manage** &gt; **Access (IAM)**, and select **Settings**.
1. From the Login session section, click the **Edit** icon ![Edit icon](../icons/icon_write.svg) from the Active sessions tile. 
1. Enter the time limit. The longest a session can last is 720 hours. 
1. Click **Save**. 


## Setting the sign out due to inactivity duration
{: #sessions-inactivity}

An inactive session is one where the user hasn't done anything on their account for the duration selected. If the inactivity sign out duration is one hour, then the user will be signed out after an hour if they haven't done anything on their account in that time. To update your user's inactive sign out sessions settings, complete the following steps.

1. In the {{site.data.keyword.cloud_notm}} console, click **Manage** &gt; **Access (IAM)**, and select **Settings**.
1. From the Login session section, click the **Edit** icon ![Edit icon](../icons/icon_write.svg) from the Sign out due to inactivity tile. 
1. Enter the time limit. The longest an inactive session can last is 24 hours. 
1. Click **Save**. 


## Setting the number of allowed concurrent sessions
{: #sessions-concurrent}

You can choose the maximum number of concurrent sessions that are allowed to your account users. Concurrent sessions are active sessions that the user is signed into at one time. Users can have multiple sessions open by using different browsers and a user can also have several logins with the {{site.data.keyword.cloud_notm}} CLI. Multiple concurrent sessions are more beneficial for parallel workloads.

<!--How much of the security information should we have here? I can't think of anywhere in the docs where we mention "attackers">
This information is from Thomas Duerr: From functional side, unlimited concurrent sessions are more beneficial for parallel workload which is the state used in the IBM Cloud today without this new restriction functionality. It's beneficial since the customer can do as much independent logins as he likes to spawn, for instance, 100 CLI applications in parallel.
From security perspective, unlimited concurrent sessions make the impact much larger if an attacker somehow becomes able to spawn sessions in the users name. When the customer likes to do high-parallel processing, he can use, without limitation, as many parallel sessions as he likes in order to get as much data process as possible.
When the attacker becomes somehow able to leverage the login, and there's no session restrictions, they can do the very same, but for their purpose and paid for by the account. When concurrent sessions are limited, attackers are restricted to the amount of allowed parallel logins to process workload.-->

1. In the {{site.data.keyword.cloud_notm}} console, click **Manage** &gt; **Access (IAM)**, and select **Settings**.
1. From the Login session section, click the **Edit** icon ![Edit icon](../icons/icon_write.svg) from the Concurrent sessions tile. 
1. Enter the time limit. Users can have an unlimited number of concurrent sessions. 
1. Click **Save**. 



