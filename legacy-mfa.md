---

copyright:

  years: 2018, 2023
lastupdated: "2023-07-21"

keywords: 

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Deprecated legacy account-based MFA
{: #legacy-mfa}

[Deprecated]{: tag-deprecated}

Legacy account-based MFA was available to accounts with classic infrastructure prior to the release of the {{site.data.keyword.cloud_notm}} MFA. This legacy offering continues to work for accounts with classic infrastructure and requires the user to provide a secondary authentication input when logging in or switching to accounts with classic infrastructure. Non-classic resources are not secured by this legacy offering. {{site.data.keyword.cloud_notm}} MFA is for customers that want to implement MFA to secure the full range of IBM Cloud offerings.
{: shortdesc}

[Classic infrastructure]{: tag-classic-inf} Account-based MFA applies only to classic infrastructure and not to other resources in your account. Unlike with {{site.data.keyword.cloud_notm}} MFA, legacy MFA options, such as security questions, are enforced only on the specific account where the MFA is enabled. If you have a different legacy MFA option set up for each account that you are a member of, you must authenticate in a different way each time that you switch accounts. 


## Account-based MFA options
{: #account-based}

An account administrator can enable any of the following legacy MFA options to be configured and used by a user in the account. Account-based MFA options are available only with classic infrastructure accounts and only protect classic infrastructure resources. This type of MFA is tied to the account. If an administrator enables a different legacy MFA option for each account that a user is a member of, the user is prompted to authenticate a different way each time that they switch accounts.

If an account requires any {{site.data.keyword.cloud_notm}} MFA, that factor overrides any legacy account-based MFA options that are enabled and set up in a user's account. Therefore, even if a user has other MFA options, such as the following set up, the user is not prompted for them at login.
{: note}

**Time-based one-time passcode authentication (TOTP)**
:   TOTP can be set up by using an authentication app. Before an account owner or administrator can enable this setting for a user on the User details page, the user must set up authentication by going to **Manage** > **Access (IAM)** > **Users** > _select a user_ > **Legacy account-based MFA** > **Set up**. If this setting is enabled for a user, they are prompted for the passcode during login. Users with access to manage their own login settings by having the User-managed login setting that is turned on from their User details page can turn on and off this MFA setting.

**Security questions**
:   Users can set up answers to the security questions that are available by going to **Manage** > **Access (IAM)** > **Users** > _select a user_ > **Legacy account-based MFA** > **Set up**. The user must set up the security questions and answers before an account owner or administrator can enable this setting on the User details page. Users with access to manage their own login settings by having the User-managed login setting that is turned on from their User details page can turn on and off this MFA setting.

**External authentication**
:   Symantec is the only external, third-party authentication option that can be ordered for a monthly cost. An account owner or administrator must order this option for a user and enable it to be used from the User details page for the user. For Symantec, the administrator must work with the user to get that user's credential ID to complete the order. Users with access to manage their own login settings by having the User-managed login setting that is turned on from their User details page can turn on and off this MFA setting.

**Password expiration**
:   The password expiration is set to never by default. When you sign up for an account, you're never required to change your password. When you set a password expiration period, you're notified of your password expiration by email 14 days before, 7 days before, and the day the password is set to expire. This option is available only to users that log in with a SoftLayer ID. To update your password expiration, you must be an account owner or have the User-managed login setting that is turned on by your account administrator on your IAM User details page.

## Enabling one-time passcode MFA for a user
{: #totp}

As an administrator or editor on the User Management service, you can enable the multifactor authentication (MFA) option that prompts a user for a time-based one-time passcode (TOTP) at login. This type of legacy account-based MFA is required only for the account where the setting is enabled and is available only for accounts with classic infrastructure.

### Before you begin
{: #totp-access}

If you have any of the following access, you can update this setting for other users in your account:

* Editor or higher role on the User management service
* You are an ancestor in the classic infrastructure hierarchy for the user and you have the Manage users classic infrastructure permission assigned

To turn on this MFA option for a user, they must first set up TOTP.
{: important}

### Setting up TOTP
{: #totp-questions-setup}

Users can set up TOTP for extra authentication at login. You must set up your TOTP before you or administrator can enable this MFA requirement for you.

To set up TOTP, complete the following steps:
1. From the console, go to Go to **Manage** > **Access (IAM)** > **Users** > _select a user_ > **Legacy account-based MFA** > **Set up**.
2. In the Time-based one-time passcode authentication seciton, click **Set up**.
3. Scan the QR code with an authentication app on your device.
4. Click **OK** when you're finished.

To remove your TOTP, click **Remove**.
{: tip}


### Enabling TOTP for a user
{: #enable-totp}

Complete the following steps to turn on TOTP MFA for a user:

1. In the {{site.data.keyword.cloud_notm}} console, click **Manage** &gt; **Access (IAM)**, and select **Users**.
2. Select a user from the list.
3. From the **User details** page in the **Manage user's login** section, set the **Time-based one-time passcode MFA** option to on.

You can manage this setting for yourself if you have the **User-managed login** setting turned on in your User detials. To check if this setting is turned on, go to **Manage > Access (IAM) > Users** and click on yourself. View the User-managed login section.
{: tip}


## Enabling security questions for a user
{: #questions}

As an administrator or editor on the User Management service, you can enable the multifactor authentication (MFA) option that prompts a user for security questions at login. This type of legacy account-based MFA is required only for the account where the setting is enabled and is available only for accounts with classic infrastructure.

### Before you begin
{: #security-question-access}

If you have any of the following types of access, you can update this setting for other users in your account:

* Editor role or higher role on the User Management service
* You are an ancestor in the classic infrastructure hierarchy for the user and you have the Manage users classic infrastructure permission assigned

You can manage this setting for yourself if you have the **User-managed login** setting turned on in your User details.

Users must set up their security questions and answers in their account before you can enable this MFA requirement.
{: important}

### Setting up security questions
{: #security-questions-setup}

Users can set up answers to three security questions for extra authentication at login. You must set up your security questions and answers before you or administrator can enable this MFA requirement for you.

To set up your security questions, complete the following steps:
1. From the console, go to **Manage** > **Access (IAM)** > **Users** > _select a user_ > **Legacy account-based MFA** > **Set up**.
2. In the Security questions section, click **Set up**.
3. Select the questions and add the answers. You must answer all three security questions.
4. Click **Save**.

To update your security questions, click **Edit**.
{: tip}

### Enabling security questions
{: #enable-security-question}

Complete the following steps to turn on MFA security questions for a user:

1. In the {{site.data.keyword.cloud}} console, click **Manage** > **Access (IAM)**, and select **Users**.
2. Select a user from the list.
3. From the **User details** page in the **Manage user's login** section, set the **Require MFA security questions at login** option to on.

If the toggle **Require MFA security questions at login** is disabled and you can't turn it on or off, you don't have access to manage the MFA factor. You must be the account owner or have the **User-managed login** setting turned on. Contact your account owner or administrator to get access to turn on the User-managed login setting. To check if User-managed login is turned on, go to **Manage > Access (IAM) > Users** and click on yourself. View the User-managed login section.
{: tip}
{: note}

## Ordering external authentication MFA for a user
{: #external}

As a master user of a legacy classic infrastructure account, you can order external authentication and enable the multifactor authentication (MFA) option for a user's login. You are charged a monthly fee for the external authentication option.

Unlike {{site.data.keyword.cloud_notm}} MFA, external authentication is account-based and require MFA for the user's login only for the account where the setting is enabled.

As of 27 May 2021, phone-based authentication is deprecated. Any related billing for previously set up phone-based authentication is removed for all users in the account, and {{site.data.keyword.cloud_notm}} replaces this feature with Symantec. To set up your account to use Symantec, complete the following steps.
{: deprecated}

### Ordering external authentication
{: #ordering}

You can order external authentication for a user if you are the master user of the account. To order external authentication, complete the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, click **Manage** > **Access (IAM)**, and select **Users**.
2. Select a user from the list.
3. From the **User details** page, select **Order external authentication** in the Manage user's login section.
4. Select **Symantec identity protection**.
    * The user must download the [Symantec VIP](https://vip.symantec.com/){: external} app and obtain a credential ID to continue with the ordering process.
5. Follow the prompts to review the price and terms before you place the order.
6. Click **Order** to finalize your selection.

After Symantec authentication is ordered, you can turn on the option for the user from the User details page.

### Setting up external authentication
{: #third-party-MFA}

To find out whether external authentication is enabled, go to **Manage** > **Access (IAM)** > **Users** > _select a user_ > **Legacy account-based MFA** > **Set up**. 

#### Setting up Symantec authentication
{: #symantec-auth}

If your account administrator chooses to order Symantec identity protection, you must work with your administrator to help them complete the order by providing your credential ID:

1. Go to [Symantec VIP](https://vip.symantec.com/){: external}.
2. Click **Download**.
3. Get your credential ID and provide the ID to your administrator to complete the order.

After your administrator orders and enables the option, you can use the app for login authentication.

### Disabling external authentication
{: #disable}

You can disable Symantec or phone-based MFA for a user at any time.

1. In the {{site.data.keyword.cloud_notm}} console, click **Manage** > **Access (IAM)**, and select **Users**.
2. Select a user from the list.
3. From the **User details** page, set the **Symantec authentication** to off.

### Canceling external authentication
{: #cancel}

You can cancel your order for external authentication at any time, if you have the correct access. You can choose to cancel immediately without any refund, or you can choose to cancel it at the one year mark from when you ordered it.

To cancel an order for external authentication, you must be an account owner or have all of the following access:

* Manage users classic infrastructure permission
* Cancel services classic infrastructure permission
* Administrator for the Support Center account management service or the view, edit, and add ticket migrated classic infrastructure permissions that are not available within the [migrated permission access groups](/docs/account?topic=account-migrated_permissions).

To cancel the external authentication order, complete the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, click **Manage** > **Access (IAM)**, and select Users.
2. Select a user from the list.
3. From the **User details** page, click **Delete** icon ![Trash icon](../icons/icon_trash.svg "Delete") for the **Symantec authentication**.
4. Select when to remove it.
5. Click **Remove**.

