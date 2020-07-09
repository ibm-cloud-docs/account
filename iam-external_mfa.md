---

copyright:

  years: 2018, 2020

lastupdated: "2020-06-09"

keywords: MFA, multifactor authentication, external authentication, order authentication, Symantec, phone-based authentication, cancel authentication order

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:external: target="_blank" .external}
{:tip: .tip}

# Ordering external authentication MFA for a user
{: #external}

As an administrator with the correct access, you can order external authentication and enable the multifactor authentication (MFA) option for a user's login. You are charged a monthly fee for the external authentication options. This type of multifactor authentication (MFA) is required only for the account where the setting is enabled unlike ID-based MFA. For more information, see [Types of multifactor authentication](/docs/account?topic=account-types).
{:shortdesc}

## Ordering external authentication
{: #ordering}

You can order external authentication for a user if you are the master user or if you have the Manage User and Add/Upgrade Services permissions.

To order external authentication, complete the following steps:

1. In the {{site.data.keyword.cloud}} console, click **Manage** &gt; **Access (IAM)**, and select **Users**.
2. Select a user from the list.
3. From the **User details** page, select **Order external authentication** in the Manage user's login section.
4. Select **Symantec identity protection** or **Phone-based identity protection**.
    * For Symantec authentication, the user must download the [Symantec VIP](https://vip.symantec.com/){: external} ![External link icon](../icons/launch-glyph.svg) app and obtain a credential ID to continue with the ordering process.
    * For phone-based authentication, you can proceed with the order, but your user must [set up their configuration](/docs/account?topic=account-external#setting-up-phone-based-authentication) before you can enable the option.
5. Based on your selection, follow the prompts to review the price and terms before you place the order.
6. Click **Order** to finalize your selection.

After Symantec authentication is ordered, you can turn on the option for the user from the User details page. And, after phone-based authentication is ordered and then configured by the user, you can turn on the option for the user from the User details page.

## Setting up external authentication
{: #third-party-MFA}

You or your account administrator can order Symantec or phone-based authentication for you for a monthly cost. For you to order external authentication, you must have the add services classic infrastructure permission. To find out whether external authentication is enabled, go to **{{site.data.keyword.avatar}}** icon ![Avatar icon](../icons/i-avatar-icon.svg) > **Profile and settings**, and select **Login settings**. 

### Setting up Symantec authentication

If your account administrator chooses to order Symantec identity protection, you must work with your administrator to help them complete the order by providing your credential ID:

1. Go to [Symantec VIP](https://vip.symantec.com/).
2. Click **Download**.
3. Get your credential ID and provide the ID to your administrator to complete the order.

After your administrator orders and enables the option, you can use the app for login authentication.

### Setting up phone-based authentication

You can set up and use phone-based identity protection after your account administrator orders and enables it.

1. Go to the **{{site.data.keyword.avatar}}** icon ![Avatar icon](../icons/i-avatar-icon.svg) > **Profile and settings**, and select **Login settings**.
2. If Phone-based MFA is disabled, click **Go to User details**.
3. In the Manage user's login section, turn on phone-based authentication.
4. To provide contact information for the authentication, click the **Edit** icon ![Edit icon](../icons/edit-tagging.svg).
5. Complete all the fields. You can specify whether to receive a phone call or a text message as the authentication method. If you want to require a PIN, select the option from the **Pin type** list, and provide the PIN you want to use.  
6. Click **Apply**.

## Disabling external authentication options
{: #disable}

You can disable Symantec or phone-based MFA for a user at any time.

1. In the console, click **Manage** &gt; **Access (IAM)**, and select **Users**.
2. Select a user from the list.
3. From the **User details** page, set the **Symantec authentication** or **Phone-based authentication** option to off.

## Cancelling external authentication options
{: #cancel}

You can cancel your order for external authentication at any time, if you have the correct access. You can choose to cancel immediately without any refund, or you can choose to cancel it at the one year mark from when you ordered it.

To cancel an order for external authentication, you must be an account owner or have all of the following access:

* Manage users classic infrastructure permission
* Cancel services classic infrastructure permission
* Administrator for the Support Center account management service or the view, edit, and add ticket migrated classic infrastructure permissions that are not available within the [migrated permission access groups](/docs/account?topic=account-migrated_permissions).

To cancel the external authentication order, complete the following steps:

1. In the console, click **Manage** &gt; **Access (IAM)**, and select Users.
2. Select a user from the list.
3. From the **User details** page, click **Delete** ![Trash icon](../icons/icon_trash.svg) for the **Symantec authentication** or **Phone-based authentication**.
4. Select when to remove it.
5. Click **Remove**.