---

copyright:
  years: 2021, 2022
lastupdated: "2022-01-25"

keywords: IBM Cloud notifications, notification preferences, user notifications, distribution list, notification distribution list

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}


# Adding users to a distribution list 
{: add-users-distribution-list}

The {{site.data.keyword.Bluemix_notm}} [notification distribution list page](/account/notifications-distribution-list){: external} provides a way for you to specify a set of email addresses or webhooks to set suitable destinations for notifications about account-wide events.
{: shortdesc}

You can manage the notification distribution list by using the {{site.data.keyword.Bluemix_notm}} console. You can create a list of up to 10 email addresses and up to 10 webhooks that can receive notifications. Emails that are added to the distribution list are notified about any event that is affecting the account. You must have the editor role or higher on the account management service to add email addresses to the distribution list. For more information, see [Assigning access to account management services](/docs/account?topic=account-account-services).

For more information about webhooks and how to add them to the distribution list, see [Adding webhooks to a distribution list](/docs/account?topic=account-webhook-distribution-list).

Email addresses that are added to the distribution list by the account owner receive notifications about any incident, maintenance, announcement, or security bulletin that appears on the account owner's [Notifications page](/notifications){: external}. 

## Adding email addresses to a distribution list in the console
{: #add-users-console}

To add emails to a distribution list, complete the following steps: 
1. Using the {{site.data.keyword.Bluemix_notm}} console, go to **Manage** > **Account** > **Notification distribution list**. 
2. Select **Add** > **Email**. 
3. Enter a name and an email address. 

    You can add up to 10 email addresses to the distribution list. Email addresses don't need to correspond to known users in {{site.data.keyword.Bluemix_notm}}, you can add any type.
    {: note}

4. Click **Add**. 

## Unsubscribing from the distribution list
{: unsubscribe-distribution-list}

To unsubscribe from the distribution list, use the link in the footer of any email that is sent from the distribution list. 
