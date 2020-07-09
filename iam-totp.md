---

copyright:

  years: 2018, 2020

lastupdated: "2020-04-16"

keywords: MFA, multifactor authentication, time-based one-time passcode, TOTP

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}

# Enabling one-time passcode MFA for a user
{: #totp}

As an administrator with the correct access, you can enable the option for a user to be prompted for a time-based one-time passcode (TOTP) at login from the User details page in the {{site.data.keyword.Bluemix}} console. This type of multifactor authentication (MFA) is required only for the account where the setting is enabled unlike ID-based MFA. For more information, see [Types of multifactor authentication](/docs/account?topic=account-types).
{:shortdesc}

## Before you begin
{: #totp-access}

If you have any of the following access, you can update this setting for other users in your account:

* Editor or higher role on the User management service
* You are an ancestor in the classic infrastructure hierarchy for the user and you have the Manage users classic infrastructure permission assigned

## Enabling TOTP for a user
{: #enable-totp}

To turn on the login setting for a user to be prompted for TOTP MFA, complete the following steps.

To turn on this MFA option for a user, he or she must first [set up TOTP](#totp-setup) from the profile Login settings page.
{: note}

1. In the {{site.data.keyword.cloud_notm}} console, click **Manage** &gt; **Access (IAM)**, and select **Users**.
2. Select a user from the list.
3. From the **User details** page in the **Manage user's login** section, set the **Time-based one-time passcode MFA** option to on.

You can manage this setting for yourself if you have the User-managed login setting enabled on your User details page.
{: tip}

## Setting up TOTP
{: #totp-setup}
