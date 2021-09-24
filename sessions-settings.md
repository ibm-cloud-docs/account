---

copyright:

  years: 2021

lastupdated: "2021-09-24"

keywords: user session, inactivity, sign out, concurrent, login session, trusted profiles

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:ui: .ph data-hd-interface='ui'}
{:terraform: .ph data-hd-interface='terraform'}


# Setting limits for login sessions
{: #iam-work-sessions}

Improve the security of your account by requiring account users to enter their login credentials at customized intervals. As an account owner or user assigned the administrator role for the Identity service, you can select the time that a user's active session can last before they need to enter their credentials again. You can also choose the duration that a user is inactive before they are signed out of their session and are required to reenter their credentials. 
{: shortdesc}

To review and end active sessions to help maintain the security of your account, see [Monitoring login sessions](/docs/account?topic=account-end-user-sessions).
{: tip}

## Before you begin
{: #work-sessions-access}

If you have the following access, you can update the settings for login sessions:

* Account owner
* Editor or administrator role on all account management services
* Editor or administrator role on IAM identity service

If a user is a member of multiple accounts, the lowest value of each setting is applied to their session. For example, let's say a user is a member of two accounts: `dev account` and `test account`. If `dev account` has a 15-minute inactivity timeout, and `test account` has a 30-minute inactivity timeout, the 15-minute inactivity timeout is applied to both accounts. 
{: note}

## Setting duration of active sessions
{: #sessions-active}
{: ui}

An active session is how long a user is continuously working in their account. How an active session is gauged also depends on the duration of your session sign out due to inactivity limit. For instance, if you set the sign out to 2 hours, then the user would need to interact with the account one time between those 2 hours. 

To update your user's active sessions settings, complete the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, click **Manage** > **Access (IAM)**, and select **Settings**.
1. From the Login session section, click the **Edit** icon ![Edit icon](../icons/icon_write.svg "Edit") from the Active sessions tile. 
1. Enter the time limit. The longest a session can last is 720 hours. 
1. Click **Save**. 

## Setting duration of active sessions by using Terraform
{: #sessions-active-terraform}
{: terraform}

An active session is how long a user is continuously working in their account. How an active session is gauged also depends on the duration of your session sign out due to the inactivity limit. For example, if you set the sign out limit to 2 hours, then the user would need to interact with the account one time within those 2 hours. 

To update your user's active sessions settings by using terraform, complete the following steps:

1. In your Terraform configuration file, find the Terraform code that you used to create the `iam_account_settings_instance`.
1. Enter the period of time in seconds in which you want a session to invalidate due to inactivity. The following valid values are supported: 
   * Any whole number in the range 900 - 7200.
   * The value `NOT_SET` can be used to use the service default instead of the account setting.
   ```terraform
   resource "ibm_iam_account_settings" "iam_account_settings_instance" {
   session_invalidation_in_seconds = "7200"
   }
   ```
   {: pre}

1. Create a Terraform execution plan.
   ```terraform
   terraform plan
   ```
   {: codeblock}

1. Update the duration of active sessions. This process might take a few minutes to complete.
   ```terraform
   terraform apply
   ```
   {: codeblock}

For more information, see the [Terraform documentation](https://registry.terraform.io/providers/IBM-Cloud/ibm/latest/docs/resources/iam_account_settings#allowed_ip_addresses). 

### Setting session duration for trusted profiles
{: #sessions-active-tp}
{: ui}

1. Click the name of the trusted profile that you want to update.
2. In the federated users section, click the **Actions** icon ![Actions icon](../icons/action-menu-icon.svg "Actions") next to the identity provider (IdP) row that you want to update.
3. In hours, add or subtract how long federated users can use this profile before their session expires.
4. Click **Save**. 

## Setting the sign out due to inactivity duration
{: #sessions-inactivity}
{: ui}

An inactive session is one where the user hasn't completed any requests that send a token for validation for the duration selected. If the sign out due to inactivity duration is 1 hour, then the user will be signed out after an hour if they haven't been active in their account in that time. To update your user's sign out due to inactivity settings, complete the following steps.

1. In the {{site.data.keyword.cloud_notm}} console, click **Manage** &gt; **Access (IAM)**, and select **Settings**.
1. From the Login session section, click the **Edit** icon ![Edit icon](../icons/icon_write.svg "Edit") from the Sign out due to inactivity tile. 
1. Enter the time limit. The longest an inactive session can last is 24 hours. 
1. Click **Save**. 

## Setting the sign out due to inactivity duration by using Terraform
{: #sessions-concurrent-}
{: terraform}

An inactive session is one where the user hasn't completed any requests that send a token for validation for the duration selected. If the sign out due to inactivity duration is 1 hour, then the user will be signed out after an hour if they haven't been active in their account in that time. To update your user's sign out due to inactivity settings, complete the following steps. 

To update your user's sign out due to inactivity duration by using terraform, complete the following steps:

1. In your Terraform configuration file, find the Terraform code that you used to create the `iam_account_settings_instance`.
1. Enter the period of time in seconds in which you want a session to invalidate due to inactivity. Supported valid values are
   * Any whole number in the range 900 - 7200.
   * Use `NOT_SET` to unset account setting and use service default.
   ```terraform
   resource "ibm_iam_account_settings" "iam_account_settings_instance" {
     session_expiration_in_seconds = "3600"
   }
   ```
   {: codeblock}

1. Create a Terraform execution plan.
   ```terraform
   terraform plan
   ```
   {: pre}

1. Update sign out due to inactivity duration. This process might take a few minutes to complete.
   ```terraform
   terraform apply
   ```
   {: pre}

For more information, see the [Terraform documentation](https://registry.terraform.io/providers/IBM-Cloud/ibm/latest/docs/resources/iam_account_settings#allowed_ip_addresses). 

## Setting the number of allowed concurrent sessions
{: #sessions-concurrent}
{: ui}

You can choose the maximum number of concurrent sessions that are allowed for your account users. Concurrent sessions are active sessions that the user is signed into at one time. Users can have multiple sessions open by using different browsers or several logins with the {{site.data.keyword.cloud_notm}} CLI. Multiple concurrent sessions are more beneficial for parallel workloads.

1. In the {{site.data.keyword.cloud_notm}} console, click **Manage** > **Access (IAM)**, and select **Settings**.
1. From the Concurrent sessions tile, click the **Edit** icon ![Edit icon](../icons/icon_write.svg "Edit"), click the Unlimited dropdown > **Limit sessions**.
1. Enter the limit. Users can have an unlimited number of concurrent sessions. 
1. Click **Save**. 

## Setting the number of allowed concurrent sessions by using Terraform
{: #sessions-concurrent-terraform}
{: terraform}

You can choose the maximum number of concurrent sessions that are allowed for your account users. Concurrent sessions are active sessions that the user is signed into at one time. Users can have multiple sessions open by using different browsers or several logins with the {{site.data.keyword.cloud_notm}} CLI. Multiple concurrent sessions are more beneficial for parallel workloads.

To update your user's allowed number of concurrent sessions by using terraform, complete the following steps:

1. In your Terraform configuration file, find the Terraform code that you used to create the `iam_account_settings_instance`.
2. Enter the period of time in seconds in which you want a session to invalidate due to inactivity. Supported valid values are
   * Any whole number greater than '0'.
   * Use `NOT_SET` to unset account setting and use service default.
   ```terraform
   resource "ibm_iam_account_settings" "iam_account_settings_instance" {
    max_sessions_per_identity = "3"
   }
   ```
   {: codeblock}

3. Create a Terraform execution plan.
   ```terraform
   terraform plan
   ```
   {: pre}

4. Update the number of allowed concurrent sessions. Note that this process might take a few minutes to complete.
   ```terraform
   terraform apply
   ```
   {: pre}

For more information, see the [Terraform documentation](https://registry.terraform.io/providers/IBM-Cloud/ibm/latest/docs/resources/iam_account_settings#allowed_ip_addresses). 
