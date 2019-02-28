---

copyright:
  years: 2015, 2018
lastupdated: "2018-11-28"

keywords: notifications, email notifications, IBM Cloud notifications, notification preferences

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:note: .note}
{:screen: .screen}
{:new_window: target="_blank"}


# Setting email preferences
{: #email-prefs}

Depending on your {{site.data.keyword.Bluemix}} account type, you can choose whether to receive email notifications about {{site.data.keyword.Bluemix}} platform unplanned events and planned events, or infrastructure email notifications about unplanned events, maintenance, and announcements. You can also choose to set notification subscriptions for classic infrastructure events.
{: shortdesc}

## Setting platform notifications
{: #setting-platform-notifications}

If you're a Lite account owner, you can choose whether to receive email notifications about {{site.data.keyword.Bluemix}} platform unplanned events, such as outages, and planned events, such as maintenance. When you set {{site.data.keyword.Bluemix_notm}} platform notifications, you receive email notifications that are associated with only the {{site.data.keyword.Bluemix_notm}} platform. You do not receive email notifications about events that are associated with {{site.data.keyword.Bluemix_notm}} services.

You can set platform email notifications only for your profile, not the account. In other words, if you switch to another account, any platform notification updates you make are scoped to your profile and not the account you switched to.

When you select to receive unplanned platform events, you get emails only about issues that can cause an outage (Sev 1). At any time, you can see all planned and unplanned events from the [Status ![External link icon](../icons/launch-glyph.svg "External link icon")](https://cloud.ibm.com/status){: new_window} page.

1. Go to the Avatar icon ![Avatar icon](../icons/i-avatar-icon.svg) &gt; **Profile and settings**.
2. Click **Notifications**.
3. Select whether to receive platform notifications for each of the categories that you want to update.

  By default, all {{site.data.keyword.Bluemix_notm}} platform notifications are turned off.
  {: tip}

4. Click **Save**.

## Setting infrastructure notifications

If you're a Pay-As-You-Go or Subscription account owner, you can choose whether to receive {{site.data.keyword.Bluemix_notm}} infrastructure email notifications about unplanned events, maintenance, and announcements. Infrastructure notifications are scoped to the account that you switched to. You can switch to another account and manage notifications for that account.

1. Go to the Avatar icon ![Avatar icon](../icons/i-avatar-icon.svg) &gt; **Profile and settings**.
2. Click **Notifications**.
3. Select whether to receive infrastructure notifications for each of the categories that you want to update.

  By default, all {{site.data.keyword.Bluemix_notm}} infrastructure notifications are turned on.
  {: tip}

4. Click **Save**.

## Setting user notifications
{: #setting-user-notifications}

Setting user notifications is available for classic infrastructure resources only. If you're an account owner, you can set notification subscriptions for users in your account. The subscriptions are for a specific set of developer services like {{site.data.keyword.autoscaling}} and Raid Alert Monitoring. When the user is subscribed to a service, they receive emails about that service.  

Users in your account receive notifications for the following types of important operational events:

  * Unplanned infrastructure issues or outages: Issues that might cause an outage based on certain conditions for specific customers.
  * Planned service or scheduled maintenance: Maintenance that is required to keep the infrastructure operating at optimal status.
  * Security vulnerabilities: The affected area is isolated. A patch is created to close the vulnerability, and tests are performed on the patch to ensure that no collateral function is affected.
  * Opened support cases: Alerts users of cases that are opened on their account.

The timing of the notification varies depending on whether the event is unplanned, planned, or scheduled. The {{site.data.keyword.BluSoftlayer_notm}} infrastructure policy is to remedy problems as quickly as possible to remove or minimize the risk of further issues that might have a larger impact. Sometimes even planned maintenance is performed with only a short advanced notification.

To set up subscription notifications for your users, complete the following steps:

  1. Go to **Manage > Account**, and select **Notifications**.
  2. Select a service from the table.
  3. In the Subscribed column, select **Yes** for the user who wants to receive notifications.

    To easily find the user you're looking for, click **Filter** and filter by given name, surname, or user name.
    {: tip}
