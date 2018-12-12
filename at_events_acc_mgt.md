---

copyright:
  years: 2016, 2018

lastupdated: "2018-10-31"

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:codeblock: .codeblock}
{:tip: .tip}
{:download: .download}


# {{site.data.keyword.cloudaccesstrailshort}} events  
{: #at_events}

As a security officer, auditor, or manager, you can use the {{site.data.keyword.cloudaccesstrailfull}} service to track how users and applications interact with the {{site.data.keyword.Bluemix}} account. 
{:shortdesc}

For example, when a user, or application logs in to the {{site.data.keyword.Bluemix_notm}}, by using a password, an API key, and authentication code, or a passcode, an {{site.data.keyword.cloudaccesstrailshort}} event is generated for each attempt. 

The {{site.data.keyword.cloudaccesstrailfull_notm}} service records user-initiated activities that change the state of a service in {{site.data.keyword.Bluemix_notm}}. For more information, see [About {{site.data.keyword.cloudaccesstrailshort}}](/docs/services/cloud-activity-tracker/activity_tracker_ov.html#activity_tracker_ov ).

To get started monitoring your user's actions, see [{{site.data.keyword.cloudaccesstrailfull_notm}}](/docs/services/cloud-activity-tracker/index.html#getting-started-with-cla). 

## Events for managing accounts
{: #account}

The following table lists the API method that generates an event when they are called:

<table>
  <caption>Actions that generate events</caption>
  <tr>
    <th>Action</th>
	  <th>Description</th>
  </tr>
  <tr>
    <td>billing.account.create</td>
	  <td>An event is generated when you provison an account and after the account ID is assigned to the account.</td>
  </tr>
  <tr>
    <td>billing.account.update</td>
	  <td>An event is generated when you update information about the account.</td>
  </tr>
  <tr>
    <td>billing.account.active</td>
	  <td>An event is generated when you verify the account, or when an event is generated when the account turns into active state.</td>
  </tr>
  <tr>
    <td>billing.account.subscription.create</td>
	  <td>An event is generated when you create a <a href="/docs/account/index.html#subscription-account">subscription account</a>.</td>
  </tr>
</table>



## Events for managing users
{: #users}

The following table lists the API method that generates an event when it is called:

<table>
  <caption>Actions that generate events</caption>
  <tr>
    <th>Action</th>
	  <th>Description</th>
  </tr>
  <tr>
    <td>billing.account.user.create</td>
	  <td>An event is generated when you send an invitation to a user to join an account. </br>The account owner is the only user in the account that can perform this action.</td>
  </tr>
  <tr>
    <td>billing.user.active</td>
	  <td>An event is generated when you activate the user in the account. </br>When the user verifies his email address, the event is generated.</td>
  </tr>
  <tr>
    <td>billing.account.user.delete</td>
	  <td>An event is generated when you remove a user from the account. </br>The account owner is the only user in the account that can perform this action.</td>
  </tr>
</table>

## Events for managing organizations
{: #org}

The following table lists the API method that generates an event when it is called:

<table>
  <caption>Action that generates events</caption>
  <tr>
    <th>Action</th>
	  <th>Description</th>
  </tr>
  <tr>
    <td>billing.account.org.create</td>
	  <td>An event is generated when you add an organization to the account.</td>
  </tr>
</table>

## Where to look for the events
{: #ui}

{{site.data.keyword.cloudaccesstrailshort}} events are available in the {{site.data.keyword.cloudaccesstrailshort}} **Dallas account domain** that is available in the {{site.data.keyword.Bluemix_notm}}. For more information, see [Viewing account events](/docs/services/cloud-activity-tracker/how-to/manage-events-ui/viewing_events.html#account_events).

{{site.data.keyword.cloudaccesstrailshort}} events are automatically forwarded to the {{site.data.keyword.cloudaccesstrailshort}} service in the same region where the action happens.
