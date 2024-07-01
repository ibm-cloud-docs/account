---

copyright:

  years: 2018, 2022

lastupdated: "2022-06-14"

keywords: MFA, multifactor authentication, external authentication, order authentication, Symantec, cancel authentication order, classic infrastructure

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Ordering external authentication MFA for a user
{: #external}

As a master user of a legacy classic infrastructure account, you can order external authentication and enable the multifactor authentication (MFA) option for a user's login. You are charged a monthly fee for the external authentication option. 
{: shortdesc}

Unlike ID-based MFA, external authentication is account-based and require MFA for the user's login only for the account where the setting is enabled. For more information, see [Types of multifactor authentication](/docs/account?topic=account-types).

As of 27 May 2021, phone-based authentication is deprecated. Any related billing for previously set up phone-based authentication is removed for all users in the account, and {{site.data.keyword.cloud_notm}} replaces this feature with Symantec. To set up your account to use Symantec, complete the following steps.
{: deprecated}

## Ordering external authentication
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

## Setting up external authentication
{: #third-party-MFA}

To find out whether external authentication is enabled, go to **{{site.data.keyword.avatar}}** icon ![Avatar icon](../icons/i-avatar-icon.svg "Avatar") > **Profile**, and select **Login settings**. 

### Setting up Symantec authentication
{: #symantec-auth}

If your account administrator chooses to order Symantec identity protection, you must work with your administrator to help them complete the order by providing your credential ID:

1. Go to [Symantec VIP](https://vip.symantec.com/){: external}.
2. Click **Download**.
3. Get your credential ID and provide the ID to your administrator to complete the order.

After your administrator orders and enables the option, you can use the app for login authentication.

## Disabling external authentication
{: #disable}

You can disable Symantec or phone-based MFA for a user at any time.

1. In the {{site.data.keyword.cloud_notm}} console, click **Manage** > **Access (IAM)**, and select **Users**.
2. Select a user from the list.
3. From the **User details** page, set the **Symantec authentication** to off.

## Canceling external authentication
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
