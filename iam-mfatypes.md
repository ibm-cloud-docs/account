---

copyright:

  years: 2018, 2025
lastupdated: "2025-03-19"

keywords: MFA, multifactor authentication, two-factor authentication, U2F, FIDO U2F, security key

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# {{site.data.keyword.cloud_notm}} multifactor authentication
{: #types}

Multifactor authentication (MFA) adds a layer of security to your account by requiring all users to authenticate by using another authentication factor beyond an ID and password. MFA is also commonly known as two-factor authentication (2FA).
{: shortdesc}

{{site.data.keyword.cloud_notm}} is associated with each users' ID and authenticates them across all accounts that they are a member of, so they authenticate only one time.

{{site.data.keyword.cloud_notm}} MFA applies to all resources in any type of account. When MFA is enabled, a user is prompted to provide a unique identifier (such as a username or email) and a one-time password (OTP) generated by an authenticator app or a hardware token. After the correct OTP is entered, access is granted to the requested resource. This type of MFA is much more secure than account-based MFA because it is not limited to classic infrastructure resources and applies to all resources within the account. It also reduces the risk of a breach because of a weak password or the use of the same password across multiple accounts.

## MFA options
{: #mfa-options}

As an administrator on the IAM Identity Service or All IAM Account Management services, you can enable MFA for the account or a specific user, and it applies to all account resources.
- You can update the MFA setting for your account by going to **Manage** > **Access (IAM)** > **Settings** > **Authentication** in the {{site.data.keyword.Bluemix}} console. For more information, see [Enabling MFA for an account](/docs/account?topic=account-enablemfa#enabling-account).
- You can update the MFA setting for a specific user in your account by going to **Manage** > **Access (IAM)** > **Users** and clicking the user whose MFA you want to update. If you are a new user, use the ID-based MFA option to ensure that your login is secure. For more information, see [Enabling MFA for an individual user](/docs/account?topic=account-enablemfa#enabling-user).

### MFA for users with an IBMid
{: #mfa-options-ibmid}

Users authenticate by using an IBMid, password, and time-based one-time passcode (TOTP). You can enable this option for all users or only nonfederated users.

### MFA for all users (IBMid and supported IdPs)
{: #mfa-options-all-users}

Users authenticate by using one of the following MFA factors. This option applies to all users, including users who are using an IBMid or an external identity provider (IdP), like App ID.
* Email-based MFA: Users authenticate by using a security passcode, which is sent by email.
* TOTP MFA: Users authenticate by using a TOTP.
* U2F MFA: Users authenticate by using a physical hardware-based security key. Based on the FIDO U2F standard, this factor offers the highest level of security.

### None
{: #mfa-none}

All users log in by using only a standard ID and password, which offers the lowest level of security. To increase the level of security for this option, you can disable logging in to the CLI with only a username and password. This way, you require an API key to log in to the CLI or users can log in with `--sso`.

Starting 3 May 2023, by default CLI logins with only a username and password are disabled for all users that have MFA set to **None**. This applies to users in new and existing accounts. Administrators can opt-out before that date in the {{site.data.keyword.cloud_notm}} console. For more information, see [Disabling CLI logins with only a password](/docs/account?topic=account-enablemfa#disabling-cli). 
{: important}
