---

copyright:
  years: 2021, 2024

lastupdated: "2024-06-08"


keywords: IBM Cloud notifications, notification preferences, email preferences, user notifications, distribution list, webhooks, Slack webhooks, Microsoft Teams webhooks, ServiceNow webhooks, SNOW

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Adding webhooks to a distribution list
{: #webhook-distribution-list}

In addition to adding email addresses, you can also add up to 10 webhooks to a [distribution list](/account/notifications-distribution-list){: external}. Account administrators can create and use webhooks to configure an application to receive asynchronous notifications whenever a platform event occurs. The registered webhooks send the information to the specified URL in the form of an HTTP POST request with a JSON payload. The content-type of the request is `application/json`.
{: shortdesc}

When you receive a notification through a webhook, a payload is being sent to your given webhook endpoint (URL), and informs you about all the details of an occurring event. See the following example:

```json
{
  "account_id": "2dd2d2de4add4a098ebd0999be5cc555",
  "body": [
    {
      "language": "en",
      "text": "<p><br />SERVICES/COMPONENTS AFFECTED:<br />- Cloudant NoSQL DB<br />- Code Engine<br />- DNS Services<br />- App ID<br />- IBM Watson Machine Learning<br />- Continuous Delivery - Toolchain<br />- MQ in IBM Cloud<br />- Hyper Protect Crypto Services<br /><br />IMPACT:<br />- Users may experience connectivity issues when trying to connect to Cloudant services.<br /><br />STATUS:<br />- 2021-05-25 14:54 UTC - INVESTIGATING - We are aware of the issue and are currently investigating. More information will be provided as it becomes available.</p>"
    }
  ],
  "category": "Incident",
  "componentNames": "Cloudant",
  "continentNames": [
    "North America",
    "Europe",
    "Asia Pacific"
  ],
  "regionNames": [
    "Washington DC",
    "London",
    "Dallas",
    "Sydney",
    "Tokyo",
    "Frankfurt"
  ],
  "regions": [
    "us-east",
    "eu-gb",
    "us-south",
    "au-syd",
    "jp-tok",
    "eu-de"
  ],
  "severity": "Severity 1",
  "sourceID": "INC3918600",
  "startTime": 1621949594,
  "state": "Investigating",
  "title": [
    {
      "language": "en",
      "text": "INVESTIGATING: IBM Cloudant - selective services  are unavailable"
    }
  ],
  "updateTime": 1621954682
}
```

## Headers
{: #header-payload}

You receive the payload with a header that you configured in the UI when you added a webhook, and with an additional version header that has a semantic version number. This version header can be used to determine the expected format of the webhook payload.

The current version header is `"IBM-Notifications-API-Version": "v2.0.0"`.

## Field values
{: #field-value-payload}

The following descriptions provide information about the field values that are being sent inside the payload:

`body`: This field describes the event that is happening on the platform and concerns you. This field contains a detailed, human readable description of the notification and can be several paragraphs long. It can also contain html formatting. This field is configured to support more languages, although only English is supported currently.

`category`: The type of the event. This can be incident, maintenance, announcement, or security bulletins.

`componentNames`: If a service is impacted, this field represents it. This can also be a global value like `Component: IBM Cloud`, not only a specific service. See the services on the [{{site.data.keyword.Bluemix_notm}} catalog page](/catalog#services){: external}.

`regions`: This field shows you the location of the event.

`severity`: This field refers to the severity of the event. This can be Severity 1, 2, 3 or 4 for incidents, high, medium, or low for maintenance, and major or minor for announcements. See the following detailed severity level descriptions:
   * **Incidents**
     * `Severity 1`: Business-critical functionality is inoperable or critical interference failed. This severity usually applies to the production environment and the inability to access services is causing a critical impact on operations.
     * `Severity 2`: Core functionality is impacted. Service is operational but causing major impact on usage.
     * `Severity 3`: Partial or noncritical disruption to functionality with minimal or isolated impact.
     * `Severity 4`: A minor issue that requires action, but does not impact functionality or usage.
   * **Maintenance**
     * `High impact`: Maintenance will, or is likely to cause service outages and disruptions.
     * `Medium impact`: Maintenance will, or is likely to cause measurable service degradation but not an actual outage.
     * `Low impact`: Maintenance will cause no service disruption during or after the maintenance window.
   * **Announcements**
     * `Major`: Important incidents such as legal notices, service deprecation, or security patches.
     * `Minor`: Informative announcements such as product enhancements.

`state`: This field is only for maintenance and notifications. See the following possible values:
   * Values for *Maintenance* states: Planned, In progress, Completed, Canceled, Failed
   * Values for *Incident* states: New issue, Investigating, Resolved

`title`: The title field tells you what the notification is about. This field is configured to support more languages, although only English is supported currently.

`startTime`, `endTime`: You can check when the event starts, and when it ends.

The `startTime` and `endTime` fields show the start time and end time of the event in Unix Coordinated Universal Time timestamps.
{: note}

Fields that are sent inside the payload can be either required or optional. Optional fields, for example `startTime`, are passed if the notification has this type of information, and aren't be passed if the notification does not have it. Required fields, for example `category`, are passed in all cases. The following table lists which fields are required and which ones are optional:

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
{: caption="Fields in a payload" caption-side="top"}

Additional fields might be added in the future without a major version change. This means that any code that is processing notifications should be prepared to ignore the fields that it does not recognize.
{: note}

## Adding webhooks to a distribution list
{: #add-webhook-distribution-list}

To add webhooks to a distribution list, complete the following steps:
1. Go to **Manage** > **Account** > **Notification distribution list** in the {{site.data.keyword.cloud}} console.
2. Click **Add**, and select **Add webhook**.
3. Enter a name identifier for your webhook and an endpoint URL, where the notifications about events are being sent when the webhook is triggered. Set up the URL that will be your own custom endpoint.

   Custom header and secure header fields are also available to set. You can specify these by clicking **Add header** or **Add secure header**. If you choose to add a secure header for credentials, they are passed encrypted with the private data. This type of header can be deleted, but cannot be edited later. You can easily edit and delete custom headers later.
   {: tip}

    If you no longer want to receive notifications, you can easily delete your webhook from the distribution list by clicking the **Actions** icon ![Actions icon](../icons/action-menu-icon.svg "Actions") > **Delete** in your webhook's row.

    You can select which {{site.data.keyword.cloud_notm}} account you use by clicking the account switcher in the console. Users in the selected account receive notifications about any events that affect the account.
    {: note}

### Sending test notifications to a webhook
{: #test-webhook}

If you are ready with the previous steps and have a configured webhook, you can test it out easily. Send a test notification to your webhook and make sure that your webhook integration is working correctly and receives the notification.

Complete the following steps to send a test notification to a webhook:
1. Go to **Manage** > **Account** > **Notification distribution list** in the {{site.data.keyword.cloud_notm}} console.
2. Select the webhook that you would like to send a test notification to, and click the **Actions** icon ![Actions](../icons/action-menu-icon.svg "Actions").
3. Click **Test** > **Send test**.
4. To resend the test notification, click **Resend test**.

## Adding Slack webhooks to a distribution list
{: #add-slack-webhook}

You can now add Slack webhooks to your distribution list and receive account-wide {{site.data.keyword.Bluemix_notm}} notifications through them.

To create a webhook, first set up an app in Slack and create the incoming webhook, which provides the unique URL where you can send the notification message text in the form of a JSON payload. You will receive the notifications in the selected Slack channel in which you installed your app. For more information, see [Sending messages using Incoming Webhooks](https://api.slack.com/messaging/webhooks){: external}.

To add a Slack webhook in the {{site.data.keyword.Bluemix_notm}} console, complete the following steps:

1. Go to **Manage** > **Account** > **Notification distribution list** in the {{site.data.keyword.cloud_notm}} console.
2. Click **Add**, and select **Slack**.
3. Enter a name for your webhook and a Slack webhook URL. The notifications are sent to this unique URL.

## Adding Microsoft Teams webhooks to a distribution list
{: #add-microsoft-teams-webhook}

Adding Microsoft Teams webhooks to your distribution list is also available for you to receive account-wide {{site.data.keyword.Bluemix_notm}} notifications.

To create a webhook in the {{site.data.keyword.Bluemix_notm}} console, first create the incoming webhook in Microsoft Teams. This allows external apps to share content in Teams channels, and provides the unique URL where you can send the notification message text in the form of a JSON payload. You receive the notifications in the selected Teams channel in which you added the incoming webhook. For more information, see [Create Incoming Webhook](https://learn.microsoft.com/en-us/microsoftteams/platform/webhooks-and-connectors/how-to/add-incoming-webhook?tabs=dotnet){: external}.

To add a Microsoft Teams webhook in the {{site.data.keyword.Bluemix_notm}} console, complete the following steps:

1. Go to **Manage** > **Account** > **Notification distribution list** in the {{site.data.keyword.cloud_notm}} console.
2. Click **Add**, and select **Microsoft Teams**.
3. Enter a name for your webhook and a Microsoft Teams webhook URL. The notifications are sent to this unique URL.

## Setting up ServiceNow webhooks
{: #set-snow-webhook}

Unlike Microsoft Teams and Slack webhook integrations, setting up a ServiceNow webhook requires configuration to be done on the webhook destination side.

First, you need to create a Scripted REST API on the ServiceNow website. After the Scripted REST API is configured, you also need to create a Scripted REST API Resource. The request method needs to be set to HTTP POST. Then, you need to provide a code for the resource to run.

When you are ready with the process and have the URL for your Scripted REST API, you can start to use it on the **{{site.data.keyword.Bluemix_notm}} Notification distribution list** page and create webhooks.

To get to know the complete ServiceNow webhook integration process, follow the instructions in the [How to Integrate Webhooks Into ServiceNow](https://www.servicenow.com/community/in-other-news/how-to-integrate-webhooks-into-servicenow/ba-p/2271745){: external} blog post. This blog walks you through the steps in detail.
