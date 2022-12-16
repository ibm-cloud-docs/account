---

copyright:

  years: 2018, 2022

lastupdated: "2022-12-16"

keywords: MFA, multifactor authentication, IBMid MFA, two-factor authentication, account MFA, time-based one-time passcode, TOTP, FIDO U2F, U2F, universal 2nd factor authentication, security key

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Enabling MFA in your account
{: #enablemfa}

As an IAM Administrator, you can choose to require multifactor authentication (MFA) for every user in the account, just users with IBMids who do not use single sign-on (SSO), or individual users.
{: shortdesc}

This document covers how to work with [ID-based MFA](/docs/account?topic=account-types#id-based), which is the recomended MFA method.
{: note}


## Before you begin
{: #considerations}

The following information is helpful to consider before you enable ID-based MFA for your account to ensure that you know how it affects all users in your account:

* Enabling MFA for all users in your account affects all members of the account. If users in your account are members of multiple {{site.data.keyword.cloud_notm}} accounts, they must enroll for MFA at their next login even if they don't intend to use resources in the account where MFA is enabled.
* API keys for users and service IDs continue to work after MFA is enabled.
* If you require the use of CLI or UI login into Cloud Foundry, you must use API keys, or SSO after MFA is enabled for the account.
* MFA for your account applies to a user's login, but does not apply to API calls. If a user has permission to make API calls to resources in your account, the user can do so without completing MFA. If the user belongs to other accounts, the user can make API calls to resources in your account by using an API key from an account that did not require MFA.
* Plan a communication and support strategy for users in your account:
   * Choose a date and time that you plan to enable MFA that results in the least impact to your business.
   * Notify your account users after you enable MFA with information on how to get set up.

When you set the ID-based account default MFA, all IBMid users in your account are prompted for IBMid MFA authentication upon login. If you have other MFA factors set up for any IBMid users in your account, they are no longer prompted for those MFA factors. For example, if you previously enabled security questions in the customer portal for your classic infrastructure resources, the MFA account setting overrides the security questions option.
{: tip}

You can also enable and disable MFA in your account on the [Verification methods and authentication factors](https://iam.cloud.ibm.com/mysecurity){: external} page by clicking **Show accounts** > **Manage your own account**.
{: note}

## Enabling MFA
{: #enabling}
{: help}
{: support}

Enabling MFA does not affect users that are already logged in because MFA takes effect only at the time of login. Make sure that you notify your account users that MFA is enabled, and describe the impact to users at their next login.

The first time that you log in to your account after MFA settings are updated, you need to verify your identity by using two different verification methods. Methods for verification include email, text, or phone call, and you can use any combination of those options to verify your identity. After you verify your identity, you set up your authentication factors. If you need to update your verification methods or authentication factors later, see [Managing verification methods and MFA factors](/docs/account?topic=account-verification-authentication).
{: note}

### Enabling MFA for an account
{: #enabling-account}

1. In the {{site.data.keyword.cloud_notm}} console, go to **Manage** > **Access (IAM)** > **Settings**.
1. Click **Authentication**.
1. Select the type of MFA that you want to enable in your account. For more information about the MFA options, see [ID-based MFA options](/docs/account?topic=account-types#id-based).

### Enabling MFA for an individual user
{: #enabling-user}

1. In the {{site.data.keyword.cloud_notm}} console, go to **Manage** > **Access (IAM)** > **Users** and select the user whose MFA you want to update.
1. Go to the Multifactor authentication section and click the **Edit** icon ![Edit icon](../icons/edit-tagging.svg "Edit").
1. Select the type of MFA to enable for the user.

   By default, **Use account default** is selected. The account default is the MFA option that is enabled at the account level. To view the account default, go to **Manage > Access (IAM) > Settings > Authentication**.
   {: note}

1. Click **Save**.

## Disabling MFA
{: #disablemfa}

Disabling MFA does not affect users that are already logged in. The action impacts all new logins.

### Disabling MFA for an account
{: #disable-account}

1. Go to **Manage** > **Access (IAM)** > **Settings** in the {{site.data.keyword.cloud_notm}} console.
1. Click **Edit** in the Authentication section.
1. Select **None**.

### Disabling MFA for an individual user
{: #disabling-user}

1. In the {{site.data.keyword.cloud_notm}} console, go to **Manage** > **Access (IAM)** > **Users** and select the user whose MFA you want to update.
1. Go to the Multifactor authentication section and click the **Edit** icon ![Edit icon](../icons/edit-tagging.svg "Edit").
1. Select **None**.
1. Click **Save**.
