---

copyright:

  years: 2018, 2023
lastupdated: "2023-04-12"

keywords: MFA, multifactor authentication, two-factor authentication, U2F, FIDO U2F, security key

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Types of multifactor authentication
{: #types}

Multifactor authentication (MFA) adds an extra layer of security to your account by requiring all users to authenticate by using another authentication factor beyond an ID and password. MFA is also commonly known as two-factor authentication (2FA).
{: shortdesc}

The following two types of MFA options might be enabled for your account:

ID-based MFA
:   ID-based MFA is the preferred method for requiring MFA in an account. This type of MFA is associated with each users' ID and authenticates them across all accounts that they are a member of, so they authenticate only one time. This type of MFA overrides the legacy account-based MFA options.

Account-based MFA
:   [Classic infrastructure]{: tag-classic-inf} Legacy MFA options, such as security questions, are enforced only on the specific account where the MFA is enabled, unlike ID-based MFA. If you have a different legacy MFA option set up for each account that you belong to, you must authenticate in a different way each time you switch accounts. These legacy MFA options are available only with classic infrastructure accounts.

For users that are members of multiple accounts, the most restrictive MFA option that is enabled in any of the accounts is the only MFA that you must satisfy. ID-based MFA is more restrictive than account-based MFA, and satisfies the authentication requirement. If an account that you are a member of enables ID-based MFA, this is the only type of MFA that you are prompted with at login.
{: note}

## ID-based MFA options
{: #id-based}

As an Administrator on the IAM Identity Service or All IAM Account Management services, you can enable ID-based MFA for the account or a specific user, and it applies to all account resources.
- You can update the MFA setting for your account by going to **Manage** > **Access (IAM)** > **Settings** > **Authentication** in the {{site.data.keyword.Bluemix}} console. For more information, see [Enabling MFA for an account](/docs/account?topic=account-enablemfa#enabling-account).
- You can update the MFA setting for a specific user in your account by going to **Manage** > **Access (IAM)** > **Users** and clicking the user whose MFA you want to update. If you are a new user, use the ID-based MFA option to ensure that your login is secure. For more information, see [Enabling MFA for an individual user](/docs/account?topic=account-enablemfa#enabling-user).

### None
{: #mfa-none}

All users log in by using only a standard ID and password, which offers the lowest level of security. To increase the level of security for this option, you can disable logging in to the CLI with only a username and password. This way, you require an API key to log in to the CLI or users can log in with `--sso`.

Starting 3 May 2023, by default CLI logins with only a username and password are disabled for all users that have MFA set to **None**. This applies to users in new and existing accounts. Administrators can opt-out before that date in the {{site.data.keyword.cloud_notm}} console. For more information, see [Disabling CLI logins with only a password](/docs/account?topic=account-enablemfa#disabling-cli)
{: important}

### MFA for users with an IBMid
{: #mfa-options-ibmid}

Users authenticate by using an IBMid, password, and time-based one-time passcode (TOTP). You can enable this option for all users or only nonfederated users.

### MFA for all users (IBMid and supported IdPs)
{: #mfa-options-all-users}

Users authenticate by using one of the following MFA factors. This option applies to all users, including users who are using an IBMid or an external identity provider (IdP), like AppID.
* Email-based MFA: Users authenticate by using a security passcode, which is sent by email.
* TOTP MFA: Users authenticate by using a TOTP.
* U2F MFA: Users authenticate by using a physical hardware-based security key. Based on the FIDO U2F standard, this factor offers the highest level of security.

## Account-based MFA options
{: #account-based}

[Classic infrastructure]{: tag-classic-inf}

An account administrator can enable any of the following legacy MFA options to be configured and used by a user in the account. These legacy MFA options are available only with classic infrastructure accounts. This type of MFA is tied to the account. If an administrator enables a different legacy MFA option for each account that a user is a member of, the user is prompted to authenticate a different way each time that they switch accounts.

If an account requires any ID-based MFA, that factor overrides any legacy account-based MFA options that are enabled and set up in a user's account. Therefore, even if a user has other MFA options, such as the following set up, the user is not prompted for them at login.
{: note}

**Time-based one-time passcode authentication (TOTP)**
:   TOTP can be set up by using an authentication app. Before an account owner or administrator can enable this setting for a user on the User details page, the user must set up authentication by going to **{{site.data.keyword.avatar}}** icon ![Avatar icon](../icons/i-avatar-icon.svg "Avatar") **> Profile > Login settings**. If this setting is enabled for a user, they are prompted for the passcode during login. Users with access to manage their own login settings by having the User-managed login setting that is turned on from their User details page can turn on and off this MFA setting.

**Security questions**
:   Users can set up answers to the security questions that are available by going to **{{site.data.keyword.avatar}}** icon ![Avatar icon](../icons/i-avatar-icon.svg "Avatar") **> Profile > Login settings**. The user must set up the security questions and answers before an account owner or administrator can enable this setting on the User details page. Users with access to manage their own login settings by having the User-managed login setting that is turned on from their User details page can turn on and off this MFA setting.

**External authentication**
:   Symantec is the only external, third-party authentication option that can be ordered for a monthly cost. An account owner or administrator must order this option for a user and enable it to be used from the User details page for the user. For Symantec, the administrator must work with the user to get that user's credential ID to complete the order. Users with access to manage their own login settings by having the User-managed login setting that is turned on from their User details page can turn on and off this MFA setting.

**Password expiration**
:   The password expiration is set to never by default. When you sign up for an account, you're never required to change your password. When you set a password expiration period, you're notified of your password expiration by email 14 days before, 7 days before, and the day the password is set to expire. This option is available only to users that log in with a SoftLayer ID. To update your password expiration, you must be an account owner or have the User-managed login setting that is turned on by your account administrator on your IAM User details page.
