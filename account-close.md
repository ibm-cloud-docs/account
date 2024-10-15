---

copyright:

  years: 2024

lastupdated: "2024-09-12"

keywords: close account, cancel account, delete account, terminate account

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}


# Closing an account
{: #account-close}

When you decide that you no longer need your {{site.data.keyword.cloud}} account, you can close the account by using the {{site.data.keyword.Bluemix_notm}} console. If you need assistance with the process, don't hesitate to [contact us](/unifiedsupport/supportcenter){: external}.
{: shortdesc}

## Step 1: Canceling all services
{: #cancel-services}

To delete a service instance, use the following steps:
1. From the {{site.data.keyword.cloud_notm}} console, click the Navigation Menu icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Resource list** to view your list of resources.
2. Expand the sections to locate the service instance that you want to delete.
3. Click the **Actions** icon ![Actions icon](../icons/action-menu-icon.svg "Actions") > **Delete** for the row.

## Step 2: Canceling all devices
{: #cancel-devices}

To cancel all devices, use the following steps:
1. From the {{site.data.keyword.cloud_notm}} console, click the menu icon ![Menu icon](../../icons/icon_hamburger.svg) > **Classic Infrastructure** > **Device List**.
1. For each device that you want to cancel, click the **Actions** icon ![Action icon](../icons/action-menu-icon.svg "Actions"), and select **Cancel device**.
1. Acknowledge that data loss might occur as a result of canceling, and then click **Cancel device**.

## Step 3: Canceling all billing items
{: #cancel-billing-items}

To cancel all billing items, use the following steps:
1. From the {{site.data.keyword.cloud_notm}} console, select **Manage** > **Billing and usage**.
1. Select **Billing items**.
1. Ensure that you are viewing all billing items.
1. For each billing item that you want to cancel, click the **Actions** icon ![Action icon](../icons/action-menu-icon.svg "Actions"), and select **Cancel billing item**.

## Closing a Pay-As-You-Go account
{: #close-account}

After the account owner cancels all services, devices, and billing items for the account, they can cancel the account. To close a Pay-As-You-Go account, go to **Manage** > **Account**, select **Account settings** in the {{site.data.keyword.cloud_notm}} console. From the account settings page, click **Close account**.

If your account has reserved instances with term remaining on the agreement or if you can't cancel resources, contact [support](/unifiedsupport/supportcenter). Reschedule any pending cancellations to terminate before you cancel the account.

When you close a Pay-As-You-Go account, all usage stops across all services that are running in your account. The usage that is accrued in the current billing period is sent in one final invoice at the close of the billing period. You might receive a final invoice after you close your account due to incurred charges from the month before closing the account.

## Closing a Subscription account
{: #close-subscription-account}

To close a Subscription account, a support case is required for account security and documentation purposes. Closing your account can't be undone, and your data is unrecoverable. The support case documents your acknowledgment that the account and its data cannot be recovered after closure.

You can request to cancel your Subscription account before the end of the term, but whether the subscription can be canceled early is at the discretion of IBM. A subscription is a contract between you and IBM that commits you to use {{site.data.keyword.cloud_notm}} for a specific term and spending amount. For more information, see [Managing subscriptions](/docs/account?topic=account-subscriptions).

To create the support case, use the following steps:
1. Go to the [Support Center](/unifiedsupport/supportcenter), and click **Create a case** in the Contact Support center.
1. Click **Account**.
1. Select the **Cancel/close/suspend** subtopic and click **Next**.
1. Add a subject title and use the template as a guide to complete the case description.

   * As noted in the template, acknowledge that you understand all services and data will be permanently removed and will not be recoverable upon account closure.

Go to the [Manage cases](/unifiedsupport/cases/manage){: external} page to track the progress or to update the support case.

## Closing an enterprise account
{: #enterprise-close}

To close an enterprise account, you must also remove all child accounts. After an account is removed, it can't be reactivated. It takes 21 days after removing an account to fully remove the account from the enterprise. The account is `SUSPENDED` for 14 days and `CANCEL_PENDING` for 7 days.

To remove a child account from an enterprise, complete the following steps:
1. From the {{site.data.keyword.cloud_notm}} console, select **Manage** > **Enterprise** > **Accounts**.
1. For each account that you want to remove, click the **Actions** icon ![Action icon](../icons/action-menu-icon.svg "Actions"), and select **Remove account**.
1. Confirm that you want to remove the account.

## Closing a Lite or Trial account
{: #cancel-account}

To close a Lite account or to end a Trial account before its expiration date, go to **Manage** > **Account**, select **Account settings** in the {{site.data.keyword.cloud_notm}} console. From the account settings page, click **Close account**.

You can reactivate your account if you upgrade to a Pay-As-You-Go or Subscription account. After an account is closed for 30 days, all data are deleted and all services are removed.
