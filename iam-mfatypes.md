---

copyright:

  years: 2018, 2021
lastupdated: "2021-06-18"

keywords: MFA, multifactor authentication, two-factor authentication, U2F, FIDO U2F, security key

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}

# Types of multifactor authentication
{: #types}

Multifactor authentication (MFA) adds an extra layer of security to your account by requiring all users to authenticate by using an additional authentication factor beyond an ID and password. This is also commonly known as two-factor authentication (2FA).
{:shortdesc}

The following two types of MFA options might be enabled for your account:

<dl>
<dt>ID-based MFA</dt>
<dd>An option that is enabled by an account owner or an administrator for the billing service in one of the accounts to which you are a member. This type of MFA is associated with your IBMid and authenticates you across all accounts to which you are a member, so you authenticate only one time.</dd>
<dt>Account-based MFA</dt>
<dd>Options such as security questions that use a time-based one-time passcode and external authentication option with Symantec. These types of MFA are specific per account. If you have a different type set up for each account that you belong to, you must authenticate in a different way each time you switch accounts. These legacy MFA options are available only with classic infrastructure accounts.</dd>
</dl>

IBMid MFA satisfies the authentication requirement so that you are not prompted for any other types of MFA even if they are enabled. So, if an account to which you are a member has this option turned on, this is the only type of MFA that you are prompted for at login. If you are a new user, use the ID-based IBMid MFA option to ensure that your login is easy and secure.
{: tip}

## ID-based MFA options
{: #id-based}

The account owner or an administrator for the billing service can enable MFA at the account level, and it applies to all account resources. You can update the MFA settings for your account from the **Manage** > **Access (IAM)** > **Settings** page in the {{site.data.keyword.Bluemix}} console.

### MFA for users with an IBMid
{: #mfa-options-ibmid}

Authenticate by using an IBMid, password, and time-based one-time passcode (TOTP). You can enable this option for all users or only non-federated users.

### MFA for all users (IBMid & supported IdPs)
{: #mfa-options-all-users}

Authenticate by using one of the following MFA factors. This option applies to users who are using either an IBMid or an external identity provider (IdP). 
  
  * Email-based MFA: Users authenticate by using a security passcode that's sent via email.
  * TOTP MFA: Users authenticate by using a TOTP.
  * U2F MFA: Users authenticate by using a physical hardware-based security key that generates a six-digit numerical code. Based on the FIDO U2F standard, this factor offers the highest level of security.

## Account-based MFA options
{: #account-based}

An account administrator must enable any of the following MFA options to be configured and used by a user in the account. These legacy MFA options are available only with classic infrastructure accounts.  This type of MFA is tied to a user's current account. If an administrator enables a different one of these MFA options for each account that a user is a member of, the user is prompted to authenticate a different way each time that they switch accounts.

If an account requires IBMid MFA for all users in the account, that IBMid MFA factor overrides any other MFA options that are enabled and set up in a user's account. Therefore, even if a user has other MFA options, such as the following set up, the user is not prompted for them at login.

<dl>
<dt>Time-based one-time passcode authentication (TOTP)</dt>
<dd>TOTP can be set up by using an authentication app. An account owner or administrator can enable this setting for a user on the User details page only if the user set up authentication on the profile Login settings page. If this setting is enabled for a user, they are prompted for the passcode during login. Users with access to manage their own login settings by having the User-managed login setting turned on from their User details page can turn it on and off.</dd>
<dt>Security questions</dt>
<dd>Users can set up answers to the security questions that are available on the profile Login settings page. The user must set up the security questions and answers before an account owner or administrator can enable this setting on the User details page. Users with access to manage their own login settings by having the User-managed login setting turned on from their User details page can turn it on and off. </dd>
<dt>External authentication</dt>
<dd>Symantec is the only external, third-party authentication option that can be ordered for a monthly cost. An account owner or administrator must order this option for a user and enable it to be used from the User details page for the user. For Symantec, the administrator must work with the user to get that user's credential ID to complete the order. Users with access to manage their own login settings by having the User-managed login setting turned on from their User details page can turn it on and off.</dd>
<dt>Password expiration</dt>
<dd>The password expiration is set to never by default. When you sign up for an account, you're never required to change your password. When you set a password expiration period, you're notified of your password expiration by email 14 days before, 7 days before, and the day the password is set to expire. This option is available only to users that log in with a SoftLayer ID. To update your password expiration, you must be an account owner or have the User-managed login setting that is enabled for you by your account administrator on your IAM User details page.
</dd>
</dl>

