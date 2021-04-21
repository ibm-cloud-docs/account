---

copyright:
  years: 2015, 2021
lastupdated: "2021-04-21"

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
{:external: target="_blank" .external}


# Setting email preferences for notifications
{: #email-prefs}

Depending on your {{site.data.keyword.Bluemix_notm}} account type, you can choose to receive email notifications about {{site.data.keyword.Bluemix_notm}} platform-related items, such as announcements, billing and usage, additional notification preferences, and ordering. You can also update your preferences to receive email notifications about resource-related items, such as incidents, maintenance, security bulletins, or resource activity on the Notification preferences page. These notifications are for only the resources you use.
{: shortdesc}

To view the Notifications preferences page, go to the **{{site.data.keyword.avatar}}** icon ![Avatar icon](../icons/i-avatar-icon.svg) in the {{site.data.keyword.Bluemix_notm}} console, and then click **Profile** > **Notification preferences**.

You can also visit the page if you click the **Notifications** icon ![Notification icon](../icons/Notification.svg) in the {{site.data.keyword.Bluemix_notm}} console. Then, click **Manage email preferences** in the upper-right corner of the page. 

If you set your email preferences but aren't receiving email notifications, make sure emails that are sent from `no_reply@cloud.ibm.com` aren't blocked or in your spam folder. See [Why am I not receiving email notifications?](/docs/account?topic=account-ts_email_notifications) for more information. 
{: tip}

## Setting platform notifications
{: #setting-platform-notifications}
{: help} 
{: support}

You can choose to receive email notifications about {{site.data.keyword.Bluemix_notm}} platform-related items across your account. When you set {{site.data.keyword.Bluemix_notm}} platform notifications, you receive email notifications that are associated with only the platform. You do not receive email notifications about events that are associated with {{site.data.keyword.Bluemix_notm}} services.

Your platform email notifications settings are tied to your profile, not the account. In other words, any changes to platform notification settings are shared across your profile in all accounts that you have access to.

  * To stay up to date with changes to the {{site.data.keyword.Bluemix_notm}} platform and products, go to **Notification preferences** > **Announcements**. To select a subcategory, set **Emails** to the on position.
  * To receive notifications about invoices, payments, subscription and promo codes, or spending and usage warnings, select **Billing and usage**. Then, click **Manage** to set up spending notifications.
  * To receive updates about the status of your infrastructure orders, select **Ordering**.  
  * To manage the notification distribution list in regard to your account, subscriptions or security and compliance alerts, click **Additional notification preferences** > **Manage**.

To quickly turn off emails for the selected account, or for all other accounts, click **Actions** in the upper-right corner of the page and select your preference.
{: tip}

## Setting resource notifications
{: #setting-resource-notifications}
{: help} 
{: support}

You can set your preferences to receive resource-related notifications for incidents, maintenance, security bulletins, and resource activity updates.  

1. In the console, go to the **{{site.data.keyword.avatar}}** icon ![Avatar icon](../icons/i-avatar-icon.svg) &gt; **Profile**.
2. Click **Notification preferences** > **Resource**.
4. Select from the following options: 

  * Receive notifications about events that can cause an outage or restrict functionality. You can receive notifications for all incident severity levels (1, 2, 3, 4) or just a subset. 
  * Receive notifications about any important maintenance that keeps the platform operating at optimal status. You can receive notifications for all impact levels (high, medium, low), or just a subset.
  * Receive notifications about security vulnerabilities and the required actions to take.
  * Receive notifications about resource activity, such as status and service updates. 

To quickly turn off emails for the selected account, or for all other accounts, click **Actions** in the upper-right corner of the page and select your preference.
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

    To easily find the user you're looking for, click **Filter** and filter by given name, surname, or user name.
    {: tip}

### Assigning required access to receive notifications
{: #required-user-notification-access}

Users that you set up for classic infrastructure notifications must also have access to the devices, network, and services that send the notifications.

To ensure that a user has the correct access, go to **Manage** > **Access (IAM)** > **Users** in the console, select their name, and then select **Classic infrastructure**. From the **Permissions** option, assign users the following classic infrastructure permissions.

| Permission Category | Required Permissions |
| ------------------- | -------------------- |
| Device              | View Hardware Details <br/> View Virtual Server Details |
| Network             | Manage Network Gateways |
| Services            | Manage Lockbox <br/> Storage Manage |
{: caption="Table 1. Required classic infrastructure permissions for receiving user notifications" caption-side="top"}

Then, go to **Devices** to assign a user access to the specific devices and device types. You can also enable future access to all devices of a certain type. For more information about setting classic infrastructure permissions, see [Managing classic infrastructure access](/docs/account?topic=account-mngclassicinfra).

## Adding users to a distribution list 
{: distribution-list}

You can manage the notification distribution list under **Additional notification preferences**. You can create a list of up to 10 email addresses that can receive account-wide notifications. Users that are added to the distribution list are notified about any event that's affecting the account. You must have the editor role or higher on the account management service to add users to the distribution list. For more information, see [Assigning access to account management services](/docs/account?topic=account-account-services).

Adding users to the distribution list is different than updating your Notification preferences. Users added to the distribution list by the account owner receive any incident, maintenance, announcement, or security bulletin that appears on the account owners [{{site.data.keyword.Bluemix_notm}} - Notifications](https://cloud.ibm.com/notifications){: external} page. 
{: note}

To add users to a distribution list, complete the following steps: 
1. Using the {{site.data.keyword.Bluemix_notm}} console, go to **Manage** > **Account**, > **Notification distribution list**. 
2. Select **Add**. 
3. Enter a name identifier and an email address. 

  You can add up to 10 email addresses to the distribution list. Users that are added don't need be IBM Cloud users. You can add any email address to the distribution list. 
  {: note}
  
4. Click **Add**. 

### Unsubscribing from the distribution list 

To unsubscribe, use the link in the footer of any email that is sent from the distribution list. 

## Adding webhooks to a distribution list 
{: webhook-distribution-list}

In addition to adding email addresses, you can also add up to 10 webhooks to a distribution list. Account administrators can create and use webhooks to configure an application to receive asynchronous notifications whenever a platform event occurs. The registered webhooks send the information to the specified URL in the form of an HTTP POST request with a JSON payload. The content-type of the request is `application/json`. 

When you receive a notification through a webhook, a payload is be sent to your given webhook endpoint (URL). See the following example:

```
{
	"notification": 
		{
			"body": [
				{
				"contentType": "text/html",
				"language": "en",
				"text": "On March 26, 2021, IBM Cloud users will no longer be allowed to create or update IAM access groups with duplicate names. As a result of this change, two access groups in the same account can not have the same name. A user will receive an error when an attempt to create an access group with a duplicate name is made. This change will not have an impact on existing access groups."
				}
			],
			"category": "Announcement",
			"severity": "Minor",
			"state": "New issue",
			"subCategory": "",
			"startTime": 1618508861,
			"endTime": 1618595261,
			"title": [
				{
				"language": "en",
				"text": "New restriction on duplicate IAM access group names"
				}
			]
			"regions": [ 
				"eu-de",    "eu-gb",
		    	"us-south", "us-east",
		    	"ca-tor",   "au-syd",
		    	"jp-tok",   "jp-osa" 
		    ],
		  	"continentNames": [ "Europe", "North America", "Asia Pacific" ],
		  	"regionNames": [ 
		  		"Frankfurt",
			    "London",
			    "Dallas",
			    "Washington DC",
			    "Toronto",
			    "Sydney",
			    "Tokyo",
			    "Osaka" 
			],
		  	"componentNames": "Cloud Platform",
		}
}
```
The payload that you receive informs you about all the details of an occurring event. 

- `text`: This field describes the event that is happening on the platform and concerns you. 
- `category`: The type of the event. This can be incident, maintenance, announcement, or security bulletins. 
- `severity`: This refers to the severity of the event. This can be severity 1, 2, 3 or 4 for incidents, high, medium, or low for maintenance, and major or minor for announcements.
- `startTime`, `endTime`: You can check when the event starts, and when it ends. 
- `regions`: This field shows you the location of the event. 

The `startTime` and `endTime` fields show the start time and end time of the event in Unix UTC timestamps. 
{: note}

Fields that are sent in the payload can be either required or optional. Optional fields, for example `startTime`, are passed if the notification has this type of information, and aren't be passed if the notification does not have it. Required fields, for example `category`, are passed in all cases. The following table lists which fields are required and which ones are optional:

| Field | Required or optional |
|--|--|
|**account_id**: account_id|Required|
|**category**: notification.category |Required|
|**title**: notification.title |Required|
|**startTime**: notification.startTime |Optional|
|**endTime**: notification.endTime |Optional|
|**updateTime**: notification.updateTime |Optional|
|**body**: notification.body|Required|
|**state**: notification.state|Optional|
|**sourceID**: notification.sourceID |Optional|
|**regions**: notification.regions|Optional|
|**continentNames**: notification.continentNames|Optional|
|**regionNames**: notification.regionNames|Optional|
|**componentNames**: notification.componentNames |Optional|
|**subCategory**: notification.subCategory|Optional|
|**severity**: notification.severity|Optional|
{: caption="Table 1. Fields in a payload" caption-side="top"}


To add webhooks to a distribution list, complete the following steps: 
1. In the {{site.data.keyword.Bluemix_notm}} console, go to **Manage** > **Account**, > **Notification distribution list**. 
2. Click **Add**, and select **Add webhook**. 
3. Enter a name identifier for your webhook and an endpoint URL, which is where notifications about events are sent, when the webhook is triggered. Before this step you need to set up the URL that will be your own custom endpoint.

   Custom header and secure header fields are also available to set. You can specify these by clicking **Add header** or **Add secure header**. If you choose to add a secure header for credentials, they are passed encrypted with the private data. This type of header can be deleted, but cannot be edited later. You can easily edit and delete custom headers later. 
  {: tip}
  
  If you no longer want to receive notifications, you can easily delete your webhook from the distribution list by clicking the **Actions icon** ![More Actions icon](../icons/action-menu-icon.svg) > **Delete** in your webhook's row. 

  You can select which {{site.data.keyword.cloud_notm}} account you use by clicking the account switcher in the console. Users in the selected account receive notifications about any events that affect the account. 
  {: note}
  


