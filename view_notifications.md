---

copyright:

  years: 2019, 2025
lastupdated: "2025-11-15"

keywords: notifications, view notifications, set notifications, iaas notifications, notification icon, header bell, bell icon, email notification history, communication history

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Viewing notifications
{: #viewing-notifications}

Access essential account information by clicking the **Notifications** icon ![Notification icon "Notifications"](../icons/Notification.svg) in the console menu bar. To help you stay up to date with the latest announcements, maintenance plans, and other impacts to your account experience, a visual indicator is displayed next to the icon when a new notification is available.
{: shortdesc}

Notifications are scoped to the specific account in which you are working. Use the list of accounts that's displayed in the console menu bar to view notifications related to other accounts you have access to.
{: tip}

* The severity or impact is listed for each notification and will vary by type.
* To access a specific notification, search or filter by notification type. To access the scoped view in the future, make sure you save the URL after your search or filter options are applied.
* Navigate to a specific notification by using the unique URL that's associated with each notification. You can save and share the URL with users in the account.
* To receive future updates about a specific type of notification, click the **Email** icon that's displayed next to each notification item in the list.

## Notification types
{: #notification-type}

The following table describes the different types of notifications that are displayed.

| Notification Type | Description |
|-------------------|-------------|
| Planned maintenance | Scheduled maintenance that is required to keep the {{site.data.keyword.cloud_notm}} platform and infrastructure operating at optimal status. |
| Security bulletins | Announcements about security vulnerabilities and the required actions. |
| Announcements | Updates on new infrastructure features and services in {{site.data.keyword.cloud_notm}}. |
| Incidents | Unexpected impacting events that can cause an outage or restrict functionality. |
| Account | Invitation email, or console notifications for inviting users to the {{site.data.keyword.cloud_notm}} platform.  |
{: caption="Notification types" caption-side="top"}

## Subscribing to email notifications
{: #subscribe-email-notifications}

You can select whether to receive email notifications about {{site.data.keyword.cloud_notm}} platform-related items, such as announcements, billing and usage, additional notification preferences, and ordering. Or, about resource-related items, such as incidents, maintenance, security bulletins, and resource activity. Additionally, if you have a Pay-As-You-Go or Subscription account, you can choose whether to receive {{site.data.keyword.cloud_notm}} infrastructure service updates about changes, such as OS reloads, assigned IPs, and image and firmware updates. For more information, see [Setting email preferences for notifications](/docs/account?topic=account-email-prefs).

You cannot set email preferences for receiving account type notifications. On the {{site.data.keyword.cloud_notm}} [Notifications page](/notifications){: external}, you can use the search field to locate an invitation or filter by the notification type called account.

Users already present in {{site.data.keyword.cloud_notm}} receives an email and a notification with an invitation link. If an email address does not correspond to a known user in {{site.data.keyword.cloud_notm}}, an invitation email gets sent to accept, but users can also choose not to accept the invitation. For more information, see [Setting email preferences for notifications](/docs/account?topic=account-email-prefs) and [Inviting users to an account](/docs/account?topic=account-iamuserinv).

The invitations expire after 30 days. New users to {{site.data.keyword.cloud_notm}} can accept an invitation only by using the invitation link that they received through email.
{: note}

## Checking the delivery status of email notifications and viewing email history
{: #view-emails-history}

On the [Communication history page](/messaging){: external}, you can check the status of all email notifications that are sent to you, and you can verify whether the emails are delivered successfully. You can also view the last 90 days of {{site.data.keyword.cloud_notm}} email history, which can help you save time by troubleshooting any delivery issues without you having to contact {{site.data.keyword.IBM_notm}} support.

To view your email notification history and check the delivery status of an {{site.data.keyword.cloud_notm}} email, complete the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, click the **Notifications** icon ![Notifications icon "Notifications"](../icons/Notification.svg) in the menu bar.
1. Click **Actions > View communication history**.
1. In the **Subject** field, enter any keyword that applies to the email that you want to check.
1. Specify the date range of the email notification, and click **Submit**.
1. Filter the email notifications by the delivery status:
   * Select **Delivered** to find emails that were successfully delivered to you.
   * Select **Not delivered** to find emails that were sent to you, but weren't delivered successfully.
   * Select **All** to find both delivered and not delivered emails with the same subject.

## Getting advanced notice for disruptive maintenance
{: #disruptive-notice-maintenance}

{{site.data.keyword.cloud_notm}} tries to limit disruptive, required maintenance for Platform as a Service (PaaS), Infrastructure as a Service (IaaS), and Software as a Service offerings. Most maintenance is done in a nondisruptive manner to avoid the impact to your business, but when disruptive maintenance is necessary, we provide as much advanced notice as possible.

### Iaas
{: #iaas-offering}

For IaaS offerings, {{site.data.keyword.cloud_notm}} provides advanced notice that's dependent on the severity of the impact. The following table defines the types and levels of the possibility of an impact.

| Possibility of impact | Definition | Advanced Notice Guidelines |
|-----------------------|------------|----------------------------|
| Emergency             | Customer Impacting Event (CIE) | a minimum of 24 hours |
| High                  | Certain, likely, or has the potential to cause an extended or brief service disruption. | a minimum of 30 days |
| Medium                | Low to moderate possibility of a brief disruption. | a minimum of 21 days |
| Low                   | None to negligible chance of a disruption or routine change. No assumed risk or a disruption that is isolated to a single customer. | offering-specific |
{: caption="IaaS offerings impact possibility definitions" caption-side="top"}

### PaaS
{: #paas-offering}

For PaaS offerings, IBM Cloud provides advanced notice that's dependent on the severity of the impact. The following table defines the types and levels of the possibility of an impact.

| Possibility of impact | Definition | Advanced Notice Guidelines |
|-----------------------|------------|----------------------------|
| Emergency             | Customer Impacting Event (CIE) | a minimum of 24 hours |
| Disruptive            | Certain, likely, or has the potential to cause an extended or brief service disruption. | a minimum of 7 days |
| Nondisruptive                | None to negligible chance of a disruption or routine change. No assumed risk or a disruption that is isolated to a single customer. | None |
{: caption="PaaS offerings impact possibility definitions" caption-side="top"}

### SaaS
{: #saas-offering}

For SaaS offerings, IBM Cloud provides advanced notice that's dependent on the severity of the impact. The following table defines the types and levels of the possibility of an impact.

| Possibility of impact | Definition | Advanced Notice Guidelines |
|-----------------------|------------|----------------------------|
| Emergency             | Customer Impacting Event (CIE) | a minimum of 24 hours |
| Disruptive            | Certain, likely, or has the potential to cause an extended or brief service disruption. | a minimum of 7 days |
| Nondisruptive         | None to negligible chance of a disruption or routine change. No assumed risk or a disruption that is isolated to a single customer. | None |
{: caption="SaaS offerings impact possibility definitions" caption-side="top"}
