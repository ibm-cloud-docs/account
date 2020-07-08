---

copyright:

  years: 2018, 2020
lastupdated: "2020-06-09"

keywords: MFA, multifactor authentication, two-factor authentication

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}

# Types of multifactor authentication
{: #types}

Multifactor authentication (MFA) adds an extra layer of security to your account by requiring all users to authenticate by using an additional authentication method beyond an ID and password. This is also commonly known as two-factor authentication (2FA).
{:shortdesc}

The following two types of MFA options might be enabled for your account:

<dl>
<dt>ID-based MFA</dt>
<dd>An option that is enabled by an account owner or an administrator for the billing service in one of the accounts to which you are a member. This type of MFA is associated with your IBMid and authenticates you across all accounts to which you are a member, so you authenticate only one time.</dd>
<dt>Account-based options</dt>
<dd>Options such as security questions that use a time-based one-time passcode and external authentication options such as Symantec and phone-based authentication. These types of MFA are specific per account. If you have a different type set up for each account that you belong to, you must authenticate in a different way each time you switch accounts. These legacy MFA options are available only with former classic infrastructure accounts.</dd>
</dl>

IBMid MFA satisfies the authentication requirement so that you are not prompted for any other types of MFA even if they are enabled. So, if an account to which you are a member has this option turned on, this is the only type of MFA that you are prompted for at login. If you are a new user, use the ID-based IBMid MFA option to ensure that your login is easy and secure.
{: tip}

## ID-based MFA option
{: #id-based}

IBMid MFA for an account requires a time-based one-time passcode in addition to a standard IBMid and password during login. This type of MFA is enabled at the account level by the account owner or an administrator for the billing service. When this feature is enabled, you are required to use the extra security standard at login, and all users that are added to your account are also required. This type of MFA applies to all account resources. You can turn it on or off from the console **Manage** > **Access (IAM)** > **Settings** page in the {{site.data.keyword.Bluemix}} console only if you are the account owner or an administrator for the billing service.

One of the benefits of IBMid MFA is that it is free and tied to your ID instead of just the specific account that you are in. If you belong to many accounts, you are required to authenticate only one time when you log in to the console. For more information about IBMid MFA, the considerations that must be reviewed before you require IBMid MFA for your account, and how to set up IBMid MFA for yourself, see [Requiring MFA for users in your account](/docs/account?topic=account-enablemfa).

## Account-based MFA options
{: #account-based}

An account administrator must enable any of the following MFA options to be configured and used by a user in the account. This type of MFA is tied to a user's current account. If an administrator enables a different one of these MFA options for each account that a user is a member of, the user is prompted to authenticate a different way each time that they switch accounts.

If an account requires IBMid MFA for all users in the account, that IBMid MFA method overrides any other MFA options that are enabled and set up in a user's account. Therefore, even if a user has other MFA options, such as the following set up, the user is not prompted for them at login.

The following legacy MFA options are available only with former classic infrastructure accounts.

<dl>
<dt>Time-based one-time passcode authentication (TOTP)</dt>
<dd>TOTP can be set up by using an authentication app. An account owner or administrator can enable this setting for a user on the User details page only if the user set up authentication on the profile Login settings page. If this setting is enabled for a user, they are prompted for the passcode during login. Users with access to manage their own login settings by having the User-managed login setting turned on from their User details page can turn it on and off.</dd>
<dt>Security questions</dt>
<dd>Users can set up answers to the security questions that are available on the profile Login settings page. The user must set up the security questions and answers before an account owner or administrator can enable this setting on the User details page. Users with access to manage their own login settings by having the User-managed login setting turned on from their User details page can turn it on and off. </dd>
<dt>External authentication</dt>
<dd>There are two external, third-party authentication options that can be ordered for a monthly cost: Symantec and phone-based authentication. An account owner or administrator must order these options for a user and enable them to be used from the User details page for the user. For Symantec, the administrator must work with the user to get that user's credential ID to complete the order. And, to set up phone-based authentication, the administrator must order it, and then the user must set it up on their User details page in order for the administrator to enable it for use. Users with access to manage their own login settings by having the User-managed login setting turned on from their User details page can turn it on and off.</dd>
<dt>Password expiration</dt>
<dd>The password expiration is set to never by default. When you sign up for an account, you're never required to change your password. When you set a password expiration period, you're notified of your password expiration by email 14 days before, 7 days before, and the day the password is set to expire. This option is available only to users that log in with a SoftLayer ID. To update your password expiration, you must be an account owner or have the User-managed login setting that is enabled for you by your account administrator on your IAM User details page.
</dd>
</dl>

