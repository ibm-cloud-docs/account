---

copyright:
  years: 2015, 2020
lastupdated: "2019-05-26"

keywords: platform notifications, email notifications, IBM Cloud notifications, notification preferences, email preferences, user notifications, infrastructure notifications

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:note: .note}
{:screen: .screen}
{:help: data-hd-content-type='help'} 
{:support: data-reuse='support'} 
{:new_window: target="_blank"}


# Setting email preferences
{: #email-prefs}

Depending on your {{site.data.keyword.Bluemix}} account type, you can choose whether to receive email notifications about {{site.data.keyword.Bluemix}} platform unplanned events and planned events, or infrastructure email notifications about unplanned events, maintenance, and announcements. You can also choose to set notification subscriptions for classic infrastructure events. These notifications are for only the services you use or the devices that you have provisioned, and if they are impacted by the event, maintenance, or announcement.
{: shortdesc}

If you set your email preferences but aren't receiving email notfications, make sure emails that are sent from `no_reply@cloud.ibm.com` aren't blocked or in your spam folder. For more information, see [Why am I not receiving email notifications?](/docs/account?topic=account-ts_email_notifications).
{: tip}

## Setting platform notifications
{: #setting-platform-notifications}
{: help} 
{: support}

You can choose whether to receive email notifications about {{site.data.keyword.Bluemix}} platform unplanned events, such as outages, and planned events, such as maintenance. When you set {{site.data.keyword.Bluemix_notm}} platform notifications, you receive email notifications that are associated with only the {{site.data.keyword.Bluemix_notm}} platform. You do not receive email notifications about events that are associated with {{site.data.keyword.Bluemix_notm}} services.

Your platform email notifications settings are tied to your profile, not the account. In other words, any changes to platform notification settings are shared across your profile in all accounts that you have access to.

When you select to receive unplanned platform events, you get emails only about issues that can cause an outage (Sev 1). At any time, you can see all planned and unplanned events from the [Status ![External link icon](../icons/launch-glyph.svg "External link icon")](https://cloud.ibm.com/status){: new_window} page.

1. Go to the **{{site.data.keyword.avatar}}** icon ![Avatar icon](../icons/i-avatar-icon.svg) &gt; **Profile and settings**.
2. Click **Notifications**.
3. Select whether to receive platform notifications for each of the categories that you want to update.

  By default, all {{site.data.keyword.Bluemix_notm}} platform notifications are turned off.
  {: tip}

4. Click **Save**.

## Setting infrastructure notifications
{: #setting-infra-notifications}
{: help} 
{: support}

If you're a user in a Pay-As-You-Go or Subscription account, you can choose whether to receive {{site.data.keyword.Bluemix_notm}} infrastructure email notifications about unplanned events, maintenance, and announcements. Infrastructure notifications settings affect only the account that you're in when you set them. You can switch to another account and separately manage notifications for that account.

1. Go to the **{{site.data.keyword.avatar}}** icon ![Avatar icon](../icons/i-avatar-icon.svg) &gt; **Profile and settings**.
2. Click **Notifications**.
3. Select whether to receive infrastructure notifications for each of the categories that you want to update.

  By default, all {{site.data.keyword.Bluemix_notm}} infrastructure notifications are turned on.
  {: tip}

4. Click **Save**.

## Setting user notifications for classic infrastructure resources
{: #setting-user-notifications}

Setting user notifications is available for classic infrastructure resources only. If you're an account owner, you can subscribe users in your account to notifications for a specific set of developer services like {{site.data.keyword.autoscaling}} and Raid Alert Monitoring. When the user is subscribed to a service, they receive emails about that service. Changes that you make for a user take effect only for future notifications. A user is not notified about events that occurred before you set up notifications.

Users in your account receive notifications for the following types of important operational events:

  * Unplanned infrastructure issues or outages: Issues that might cause an outage based on certain conditions for specific customers.
  * Planned service or scheduled maintenance: Maintenance that is required to keep the infrastructure operating at optimal status.
  * Security vulnerabilities: The affected area is isolated. A patch is created to close the vulnerability, and tests are performed on the patch to ensure that no collateral function is affected.

The timing of the notification varies depending on whether the event is unplanned, planned, or scheduled. The {{site.data.keyword.BluSoftlayer_notm}} infrastructure policy is to remedy problems as quickly as possible to remove or minimize the risk of further issues that might have a larger impact. Sometimes even planned maintenance is performed with only a short advanced notification.

To set up subscription notifications for your users, complete the following steps:

  1. Go to **Manage > Account**, and select **Notifications**.
  2. Select a service from the table.
  3. In the Subscribed column, select **Yes** for the user who wants to receive notifications.

    To easily find the user you're looking for, click **Filter** and filter by given name, surname, or user name.
    {: tip}

### Assigning required access to receive notifications
{: #required-user-notification-access}

Users that you set up for classic infrastructure notifications must also have access to the devices, network, and services that send the notifications.

To ensure that a user has the correct access, go to **Manage** > **Access (IAM)** > **Users**, select their name, and then select **Classic infrastructure**. From the **Permissions** option, assign users the following classic infrastructure permissions.

| Permission Category | Required Permissions |
| ------------------- | -------------------- |
| Device              | View Hardware Details <br/> View Virtual Server Details |
| Network             | Manage Network Gateways |
| Services            | Manage Lockbox <br/> Storage Manage |
{: caption="Table 1. Required classic infrastructure permissions for receiving user notifications" caption-side="top"}

Then, go to **Devices** to assign a user access to the specific devices and device types. You can also enable future access to all devices of a certain type. For more information about setting classic infrastructure permissions, see [Managing classic infrastructure access](/docs/iam?topic=iam-mngclassicinfra#mngclassicinfra).
