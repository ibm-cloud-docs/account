---

copyright:
  years: 2021
lastupdated: "2021-10-11"

keywords: IBM Cloud notifications, notification preferences, user notifications, distribution list, notification distribution list

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:note: .note}
{:screen: .screen}
{:help: data-hd-content-type='help'} 
{:support: data-reuse='support'} 
{:external: target="_blank" .external}

# Adding users to a distribution list 
{: add-users-distribution-list}

The {{site.data.keyword.Bluemix_notm}} notification distribution list provides a way for you to specify a set of email addresses or webhooks to set suitable destinations for notifications about account-wide events.
{: shortdesc}

You can manage the notification distribution list by using the {{site.data.keyword.Bluemix_notm}} console. You can create a list of up to 10 email addresses and up to 10 webhooks that can receive notifications. Emails that are added to the distribution list are notified about any event that is affecting the account. You must have the editor role or higher on the account management service to add email addresses to the distribution list. For more information, see [Assigning access to account management services](/docs/account?topic=account-account-services).

For more information about webhooks and how to add them to the distribution list, see [Adding webhooks to a distribution list](/docs/account?topic=account-webhook-distribution-list).

Adding users to the distribution list is different than updating your notification preferences. Users added to the distribution list by the account owner receive any incident, maintenance, announcement, or security bulletin that appears on the account owners [{{site.data.keyword.Bluemix_notm}} - Notifications](https://cloud.ibm.com/notifications){: external} page. 
{: note}

## Adding users to a distribution list in the console
{: #add-users-console}

To add users to a distribution list, complete the following steps: 
1. Using the {{site.data.keyword.Bluemix_notm}} console, go to **Manage** > **Account** > **Notification distribution list**. 
2. Select **Add**. 
3. Enter a name identifier and an email address. 

   You can add up to 10 email addresses to the distribution list. Users that are added don't need be {{site.data.keyword.Bluemix_notm}} users. You can add any email address to the distribution list. 
   {: note}
  
4. Click **Add**. 

## Unsubscribing from the distribution list
{: unsubscribe-distribution-list}

To unsubscribe from the distribution list, use the link in the footer of any email that is sent from the distribution list. 
