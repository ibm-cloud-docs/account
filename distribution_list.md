---

copyright:
  years: 2021, 2022
lastupdated: "2022-09-23"

keywords: IBM Cloud notifications, notification preferences, user notifications, distribution list, notification distribution list

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Adding users to a notification distribution list
{: #add-users-distribution-list}

The {{site.data.keyword.Bluemix_notm}} [notification distribution list page](/account/notifications-distribution-list){: external} provides a way for you to specify a set of email addresses or webhooks to set suitable destinations for notifications about account-wide events.
{: shortdesc}

You can manage the notification distribution list by using the {{site.data.keyword.Bluemix_notm}} console. You can create a list of up to 10 email addresses and up to 10 webhooks that can receive notifications. Emails that are added to the distribution list are notified about any event that is affecting the account. You must have the editor role or higher on the account management service to add email addresses to the distribution list. For more information, see [Assigning access to account management services](/docs/account?topic=account-account-services).

For more information about webhooks and how to add them to the distribution list, see [Adding webhooks to a distribution list](/docs/account?topic=account-webhook-distribution-list).

Email addresses that are added to the distribution list by the account owner receive notifications about any incident, maintenance, announcement, or security bulletin that appears on the account owner's [Notifications page](/notifications){: external}.

## Adding email addresses to a notification distribution list in the console
{: #add-users-console}

To add emails to a notification distribution list, complete the following steps:
1. Using the {{site.data.keyword.Bluemix_notm}} console, go to **Manage** > **Account** > **Notification distribution list**.
2. Select **Add** > **Email**.
3. Enter a name and an email address.

    You can add up to 10 email addresses to the distribution list. Email addresses don't need to correspond to known users in {{site.data.keyword.Bluemix_notm}}, you can add any type.
    {: note}

4. Click **Add**.

## Unsubscribing from the distribution list
{: #unsubscribe-distribution-list}

To unsubscribe from the distribution list, use the link in the footer of any email that is sent from the distribution list.

## Enabling {{site.data.keyword.en_short}} for the notification distribution list
{: #event-notifications-distribution-list}

With {{site.data.keyword.en_full}}, you can choose to deliver your notifications to different destinations, including email, SMS, or webhooks. {{site.data.keyword.en_short}} is an alternative to the notification distribution list. It provides a way for you to be notified about critical events that occur in your account, and manage your notifications at scale. For more information, see [Getting started with Event Notifications](/docs/event-notifications?topic=event-notifications-getting-started).

When an event of interest occurs on the {{site.data.keyword.Bluemix_notm}} platform and an event is generated, the notification distribution list communicates with a connected {{site.data.keyword.en_short}} instance to forward a notification to the supported destination. For more information about supported {{site.data.keyword.en_short}} destinations, see [Event destinations](/docs/event-notifications?topic=event-notifications-en-destination).

## Adding an {{site.data.keyword.en_short}} instance to the notification distribution list
{: #event-notifications-add-ui}

Before you can add any {{site.data.keyword.en_short}} instance to the notification distribution list, make sure that you already have an [{{site.data.keyword.en_short}} service instance](/catalog/services/event-notifications){: external} that is in the same account as the distribution list.

If you don't have an {{site.data.keyword.en_short}} service instance, see [Create an Event Notifications service instance](/docs/event-notifications?topic=event-notifications-en-create-en-instance).

To add an existing {{site.data.keyword.en_short}} service instance to the notification distribution list, complete the following steps:

1. Using the {{site.data.keyword.Bluemix_notm}} console, go to **Manage** > **Account** > **Notification distribution list**.
1. Click **Add** > **{{site.data.keyword.en_short}}**.
1. Select an {{site.data.keyword.en_short}} service instance from the {{site.data.keyword.en_short}} instance list. If you don't have an {{site.data.keyword.en_short}} service instance that you can connect to your account, you can create one in the [{{site.data.keyword.Bluemix_notm}} catalog](/catalog/services/event-notifications){: external}.
1. Click **Add**.

You cannot add an {{site.data.keyword.en_short}} service instance to the notification distribution list that is already configured.
{: note}

## Deleting an {{site.data.keyword.en_short}} instance

You can delete any {{site.data.keyword.en_short}} instance that you added to the notification distribution list by completing the following steps:

1. Select the {{site.data.keyword.en_short}} service instance that you want to delete from the notification distribution list, and click the **Actions** icon ![Actions](../icons/action-menu-icon.svg "Actions").
1. Click **Delete**.
