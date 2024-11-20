---

copyright:
  years: 2019, 2024
lastupdated: "2024-11-19"

keywords: platform notifications, email notifications, IBM Cloud notifications, notification preferences, email preferences, user notifications, infrastructure notifications

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}


# Setting email preferences for notifications
{: #email-prefs}

{{site.data.keyword.cloud}} users can choose to receive email notifications about {{site.data.keyword.cloud_notm}} platform-related items, such as announcements, billing and usage, additional notification preferences, and ordering. Users can also update their preferences to receive email notifications about resource-related items, such as incidents, maintenance, security bulletins, or resource activity on the [Notification preferences page](/user/notifications){: external}. These notifications are for only the resources in use.
{: shortdesc}

To view the Notifications preferences page, go to the **Avatar** icon ![Avatar icon](../icons/i-avatar-icon.svg "Avatar") in the {{site.data.keyword.cloud_notm}} console, and then click **Profile > Notification preferences**.

You can also view the page if you click the **Notifications** icon ![Notifications icon](../icons/Notification.svg "Notifications") in the console, and then click **Actions > View notification preferences**.

If you set your email preferences but aren't receiving email notifications, make sure emails that are sent from `no_reply@cloud.ibm.com` aren't blocked or in your spam folder. See [Why am I not receiving email notifications?](/docs/account?topic=account-ts_email_notifications) for more information.
{: tip}

## Setting platform notifications
{: #setting-platform-notifications}
{: help}
{: support}

You can choose to receive email notifications about {{site.data.keyword.cloud_notm}} platform-related items across your account. When you set platform notifications, you receive email notifications that are associated with only the platform. You do not receive email notifications about events that are associated with {{site.data.keyword.cloud_notm}} services.

Your platform email notifications settings are tied to your account.
{: note}

1. In the console, go to the **Avatar** icon ![Avatar icon](../icons/i-avatar-icon.svg "Avatar") > **Profile**.
2. Click **Notification preferences** > **Platform**.

    * To stay up to date with changes to the {{site.data.keyword.cloud_notm}} platform and products, go to **Notification preferences** > **Announcements**. To select a subcategory, turn **Emails** on, or off.
    * To receive notifications about invoices, payments, subscription and promo codes, or spending and usage warnings, go to **Manage** > **Billing and usage** > **Manage** in the console to set up spending notifications.

    You can only set up email spending notifications if you have a Pay-As-You-Go or Subscription account.
    {: note}

    * To receive updates about the status of your infrastructure orders, select **Ordering**.
    * To manage the notification distribution list in regard to your account, subscriptions, security and compliance alerts or marketing communications, click **Additional notification preferences** > **Manage**.
    * By default, all platform notifications are turned off.

To quickly turn off emails for the selected account or for all other accounts, click **Actions**, and select your preference.
{: tip}

## Setting resource notifications
{: #setting-resource-notifications}
{: help}
{: support}

You can set your preferences to receive resource-related notifications for incidents, maintenance, security bulletins, and resource activity updates.

1. In the console, go to the **Avatar** icon ![Avatar icon](../icons/i-avatar-icon.svg "Avatar") > **Profile**.
2. Click **Notification preferences** > **Resource**.
3. Select from the following options:
    * Receive notifications about events that can cause an outage or restrict functionality. You can receive notifications for all incident severity levels (1, 2, 3, 4) or just a subset.
    * Receive notifications about any important maintenance that keeps the platform operating at optimal status. You can receive notifications for all impact levels (high, medium, low), or just a subset.
    * Receive notifications about security vulnerabilities and the required actions to take.
    * Receive notifications about resource activity, such as status and service updates.
    * By default, all {{site.data.keyword.Bluemix_notm}} resource notifications are turned off.

To quickly turn off emails for the selected account or for all other accounts, click **Actions**, and select your preference.
{: tip}

## Setting user notifications for classic infrastructure resources
{: #setting-user-notifications}

Setting user notifications is available for classic infrastructure resources only. If you're an account owner, you can subscribe users in your account to notifications for a specific set of developer services like {{site.data.keyword.autoscaling}} and Raid Alert Monitoring. When the user is subscribed to a service, they receive emails about that service. Changes that you make for a user take effect only for future notifications. A user is not notified about events that occurred before you set up notifications.

Users in your account receive notifications for the following types of important operational events:

* Unplanned infrastructure issues or outages: Issues that might cause an outage based on certain conditions for specific customers.
* Planned service or scheduled maintenance: Maintenance that is required to keep the infrastructure operating at optimal status.
* Security vulnerabilities: The affected area is isolated. A patch is created to close the vulnerability, and tests are performed on the patch to ensure that no collateral function is affected.

The timing of the notification varies depending on whether the event is unplanned, planned, or scheduled. The {{site.data.keyword.BluSoftlayer_notm}} infrastructure policy is to remedy problems as quickly as possible to remove or minimize the risk of further issues that might have a larger impact. Sometimes even planned maintenance is performed with only a short advanced notification.

To set up subscription notifications for your users, complete the following steps:

1. In the console, go to **Manage > Account**, and select **Subscriptions**.
2. Select a service from the table.
3. In the Subscribed column, select **Yes** for the user who wants to receive notifications.

You can also set up subscriptions under **Additional notification preferences** category.

To easily find the user you're looking for, click **Filter** and filter by given name, surname, or username.
{: tip}

### Assigning required access to receive notifications
{: #required-user-notification-access}

Users that you set up for classic infrastructure notifications must also have access to the devices, network, and services that send the notifications.

To ensure that a user has the correct access, go to **Manage** > **Access (IAM)** > **Users** in the console, and select the user's name > **Classic infrastructure**. From the **Permissions** option, assign users the following classic infrastructure permissions.

| Permission Category | Required Permissions |
| ------------------- | -------------------- |
| Device              | View Hardware Details  \n View Virtual Server Details |
| Network             | Manage Network Gateways |
| Services            | Storage Manage |
{: caption="Table 1. Required classic infrastructure permissions for receiving user notifications" caption-side="top"}

Then, go to **Devices** to assign a user access to the specific devices and device types. You can also enable future access to all devices of a certain type. For more information about setting classic infrastructure permissions, see [Managing classic infrastructure access](/docs/account?topic=account-mngclassicinfra).

## Managing invitation notifications
{: #invite-notifications}

Users can receive an invitation link in their notifications and by email to join an account if they are already members of {{site.data.keyword.Bluemix_notm}}. Users only with the following types of access can invite others to the {{site.data.keyword.Bluemix_notm}} platform.

* Account owner
* An IAM access policy with the Editor role or higher on the user management account management service
* The Manage Users classic infrastructure permission to add users

On the [Notifications page](/notifications){: external}, search for an invitation or filter by the notification type called account. You can't set email preferences for receiving account type notifications.

Active users receive an email and a notification with an invitation link. If an email address does not correspond to a known user, an invitation email is sent to accept, but users can choose not to accept the invitation. For more information, see [Viewing notifications](/docs/account?topic=account-viewing-cloud-status#viewing-notifications) and [Inviting users to an account](/docs/account?topic=account-iamuserinv).

The invitations expire after 30 days. New users can accept an invitation only by using the invitation link that they received through email.
{: note}


## Managing marketing communications
{: #marcom-notifications}

You might receive notifications about significant technical enhancements, changes to the terms of service, plan changes, pricing changes, and the future removal of a product from the {{site.data.keyword.cloud_notm}} catalog. With a few exceptions, these announcements are available on the [{{site.data.keyword.cloud_notm}} blog](https://www.ibm.com/blog/announcements/){: external}.

Use the following steps to update your preferences:

1. Log in to the [{{site.data.keyword.IBM_notm}} Privacy Preference Center](https://myibm.ibm.com/profile/dataprivacypreferences/consent/us-en){: external} by using your {{site.data.keyword.cloud_notm}} credentials. The toggle indicates whether your entered credential is your preferred method of contact.
1. Click **Next**.
1. Deselect **Public cloud** to stop marketing communications.
1. Click **Save**.
