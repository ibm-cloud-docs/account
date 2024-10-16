---

copyright:

  years: 2024

lastupdated: "[{LAST_UPDATED_DATE}]"

keywords: close account, cancel account, delete account, terminate account

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}


# Closing an account
{: #account-close}

Closing an {{site.data.keyword.cloud}} account is as simple as the account owner or administrator performing a few account clean-up tasks and then closing the account in the {{site.data.keyword.Bluemix_notm}} console. If you need assistance with the process, don't hesitate to [contact {{site.data.keyword.Bluemix_notm}} support](/unifiedsupport/supportcenter){: external}.
{: shortdesc}

## Deleting resources
{: #cancel-services}

To delete your resources, use the following steps:
1. Click the Navigation Menu icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Resource list** to view your list of resources.
2. Expand the category in which the specific resource is listed.
3. Click the **Actions** icon ![Actions icon](../icons/action-menu-icon.svg "Actions") > **Delete**.

## Canceling Classic Infrastructure devices
{: #cancel-devices}

To cancel your Classic Infratructure devices, use the following steps:
1. Click the menu icon ![Menu icon](../../icons/icon_hamburger.svg) > **Classic Infrastructure** > **Device List**.
1. For each device that you want to cancel, click the **Actions** icon ![Action icon](../icons/action-menu-icon.svg "Actions"), and select **Cancel device**.
1. Acknowledge that data loss might occur as a result of canceling, and then click **Cancel device**.

## Canceling billing items
{: #cancel-billing-items}

To cancel all billing items, use the following steps:
1. Click **Manage** > **Billing and usage**.
1. Click **Billing items**, and then make sure you're viewing all the billing items for the account.
1. For each billing item that you want to cancel, click the **Actions** icon ![Action icon](../icons/action-menu-icon.svg "Actions"), and select **Cancel billing item**.

## Closing a Pay-As-You-Go account
{: #close-account}

When you close a Pay-As-You-Go account, all resource usage in the account stops. The usage that is accrued in the current billing period is sent in one final invoice at the close of the billing period. You might receive a final invoice after you close your account due to incurred charges from the month before closing the account.

1. Go to **Manage** > **Account**.
1. Click **Account settings** > **Close account**.

If your account has reserved instances with term remaining on the agreement or if you can't cancel resources, contact [support](/unifiedsupport/supportcenter). Reschedule any pending cancellations to terminate before you cancel the account.

## Closing a Subscription account
{: #close-subscription-account}

To close a Subscription account, you're required to submit a support case for account security and documentation purposes. Closing your account can't be undone, and your data is unrecoverable. The support case documents your acknowledgment that the account and its data cannot be recovered after closure.

You can request to cancel your Subscription account before the end of the term, but whether the subscription can be canceled early is at the discretion of {{site.data.keyword.IBM_notm}}. A subscription is a contract between you and {{site.data.keyword.IBM_notm}} that commits you to use {{site.data.keyword.cloud_notm}} for a specific term and spending amount. For more information, see [Managing subscriptions](/docs/billing-usage?topic=billing-usage-subscriptions).

To create the support case that's used for your account closure request, complete the following steps:
1. Click the **Help** icon ![Help icon](../icons/help.svg "Help") > **Support center**.
1. From the Contact Support section, click **Create a case**.
1. Select **Account** from the category options.
1. Select **Cancel/close/suspend** from the list of subtopics, and click **Next**.
1. Add a subject title and use the template as a guide to complete the case description. As noted in the template, acknowledge that you understand all services and data will be permanently removed and will not be recoverable upon account closure.

Go to the [Manage cases](/unifiedsupport/cases/manage){: external} page in the Support center to track the progress or to update the support case.

## Closing an enterprise account
{: #enterprise-close}

To close an enterprise account, you're required to remove all child accounts that are in the enterprise account. After an account is closed, it can't be reactivated. It takes 21 days after removing an account to fully remove the account from the enterprise. The account is `SUSPENDED` for 14 days and `CANCEL_PENDING` for 7 days.

To remove a child account from an enterprise, complete the following steps:
1. Click **Manage** > **Enterprise** > **Accounts**.
1. For each child account, click the **Actions** icon ![Action icon](../icons/action-menu-icon.svg "Actions"), and select **Remove account**.
1. Confirm that you want to remove the account.

## Closing a Lite or Trial account
{: #cancel-account}

1. Go to **Manage** > **Account**. 
1. Click **Account settings** > **Close account**.

You can reactivate your account if you upgrade to a Pay-As-You-Go or Subscription account. After an account is closed for 30 days, all data are deleted and all services are removed.