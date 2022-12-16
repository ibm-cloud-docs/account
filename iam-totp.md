---

copyright:

  years: 2018, 2022

lastupdated: "2022-12-16"

keywords: MFA, multifactor authentication, time-based one-time passcode, TOTP

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Enabling one-time passcode MFA for a user
{: #totp}

As an administrator or editor on the User Management service, you can enable the multifactor authentication (MFA) option that prompts a user for a time-based one-time passcode (TOTP) at login. This type of legacy account-based MFA is required only for the account where the setting is enabled and is available only for accounts with classic infrastructure.
{: shortdesc}

For more information about your MFA options, see [Types of multifactor authentication](/docs/account?topic=account-types).

## Before you begin
{: #totp-access}

If you have any of the following access, you can update this setting for other users in your account:

* Editor or higher role on the User management service
* You are an ancestor in the classic infrastructure hierarchy for the user and you have the Manage users classic infrastructure permission assigned

To turn on this MFA option for a user, they must first set up TOTP. For more information, see [Setting up TOTP](/docs/account?topic=account-totp#totp-setup).
{: important}

## Setting up TOTP
{: #security-questions-setup}

Users can set up TOTP for extra authentication at login. You must set up your TOTP before you or administrator can enable this MFA requirement for you.

To set up TOTP, complete the following steps:
1. From the console, go to Go to **{{site.data.keyword.avatar}}** icon ![Avatar icon](../icons/i-avatar-icon.svg "Avatar") > **Profile and settings**, and select **Login settings**.
2. In the Time-based one-time passcode authentication seciton, click **Set up**.
3. Scan the QR code with an authentication app on your device.
4. Click **OK** when you're finished.

To remove your TOTP, click **Remove**.
{: tip}


## Enabling TOTP for a user
{: #enable-totp}

Complete the following steps to turn on TOTP MFA for a user:

1. In the {{site.data.keyword.cloud_notm}} console, click **Manage** &gt; **Access (IAM)**, and select **Users**.
2. Select a user from the list.
3. From the **User details** page in the **Manage user's login** section, set the **Time-based one-time passcode MFA** option to on.

You can manage this setting for yourself if you have the **User-managed login** setting turned on in your User detials. To check if this setting is turned on, go to **Manage > Access (IAM) > Users** and click on yourself. View the User-managed login section.
{: tip}
