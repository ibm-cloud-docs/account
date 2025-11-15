---

copyright:

  years: 2018, 2025
lastupdated: "2025-11-15"

keywords:

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}



# Activity tracking events for catalog management
{: #at_events_cm}



{{site.data.keyword.cloud_notm}} services, such as catalog management, generate activity tracking events.
{: shortdesc}

Activity tracking events report on activities that change the state of a service in {{site.data.keyword.cloud_notm}}. You can use the events to investigate abnormal activity and critical actions and to comply with regulatory audit requirements.

You can use {{site.data.keyword.atracker_full_notm}}, a platform service, to route auditing events in your account to destinations of your choice by configuring targets and routes that define where activity tracking events are sent. For more information, see [About {{site.data.keyword.atracker_full_notm}}](/docs/atracker?topic=atracker-about).

You can use {{site.data.keyword.logs_full_notm}} to visualize and alert on events that are generated in your account and routed by {{site.data.keyword.atracker_full_notm}} to an {{site.data.keyword.logs_full_notm}} instance.

## Locations where activity tracking events are sent by {{site.data.keyword.atracker_full_notm}}
{: #atracker-locations-cm}



Catalog management sends activity tracking events by {{site.data.keyword.atracker_full_notm}} in the regions that are indicated in the following table.

| Dallas (`us-south`) | Washington (`us-east`)  | Toronto (`ca-tor`) | Sao Paulo (`br-sao`) |
|---------------------|-------------------------|-------------------|----------------------|
| [No]{: tag-red} | [No]{: tag-red} | [No]{: tag-red} | [No]{: tag-red} |
{: caption="Regions where activity tracking events are sent in Americas locations" caption-side="top"}
{: #atracker-table-1}
{: tab-title="Americas"}
{: tab-group="atracker"}
{: class="simple-tab-table"}
{: row-headers}

| Tokyo (`jp-tok`)    | Sydney (`au-syd`) |  Osaka (`jp-osa`) | Chennai (`in-che`) |
|---------------------|------------------|------------------|--------------------|
| [No]{: tag-red} | [No]{: tag-red} | [No]{: tag-red} | [No]{: tag-red} |
{: caption="Regions where activity tracking events are sent in Asia Pacific locations" caption-side="top"}
{: #atracker-table-2}
{: tab-title="Asia Pacific"}
{: tab-group="atracker"}
{: class="simple-tab-table"}
{: row-headers}

| Frankfurt (`eu-de`)  | London (`eu-gb`) | Madrid (`eu-es`) |
|---------------------------------------------------------------|---------------------|------------------|
| [Yes]{: tag-green} | [No]{: tag-red} | [No]{: tag-red} |
{: caption="Regions where activity tracking events are sent in Europe locations" caption-side="top"}
{: #atracker-table-3}
{: tab-title="Europe"}
{: tab-group="atracker"}
{: class="simple-tab-table"}
{: row-headers}

## Viewing activity tracking events for catalog management
{: #at-viewing}



You can use {{site.data.keyword.logs_full_notm}} to visualize and alert on events that are generated in your account and routed by {{site.data.keyword.atracker_full_notm}} to an {{site.data.keyword.logs_full_notm}} instance.

### Launching {{site.data.keyword.logs_full_notm}} from the Observability page
{: #log-launch-standalone-cm}



For information on launching the {{site.data.keyword.logs_full_notm}} UI, see [Launching the UI in the {{site.data.keyword.logs_full_notm}} documentation.](/docs/cloud-logs?topic=cloud-logs-instance-launch)

## Events for managing private catalogs
{: #at_actions_private_catalog}



The following table lists the actions that generate private catalog management events:

| Action             | Description      |
|--------------------|------------------|
| `globalcatalog-collection.instance.read`| An event is generated when you view a catalog.|
| `globalcatalog-collection.instance.update`| An event is generated when you update a catalog. |
| `globalcatalog-collection.instances.list`| An event is generated when you get a list of the catalogs in an account.|
{: caption="Actions that generate events for managing private catalogs" caption-side="bottom"}

## Events for managing products in a private catalog
{: #at_actions_manage_product}

The following table lists the actions that generate events for managing products in a private catalog:

| Action             | Description      |
|--------------------|------------------|
| `globalcatalog-collection.offerings.list`          |  An event is generated when you get a list of the products in a catalog.    |
| `globalcatalog-collection.offering.read`           | An event is generated when you view a product in a catalog.      |
| `globalcatalog-collection.offering.create`         | An event is generated when you create a product.          |
| `globalcatalog-collection.offering.update`         | An event is generated when you update a product.          |
| `globalcatalog-collection.offering.delete`         | An event is generated when you delete a product.          |
{: caption="Actions that generate events for managing products in a private catalog" caption-side="bottom"}

## Events for managing catalog settings at the account level
{: #at_actions_manage_settings}

The following table lists the actions that generate events for managing catalog settings at the account level:

| Action             | Description      |
|--------------------|------------------|
| `globalcatalog-collection.account-settings.read`   | An event is generated when you view the account settings.   |
| `globalcatalog-collection.account-settings.update` | An event is generated when you update the account settings. |
{: caption="Actions that generate events for managing catalog settings at the account level" caption-side="bottom"}

## Events for managing catalog settings in enterprise accounts
{: #at_actions_manage_enterprise}

The following table lists the actions that generate events for managing catalog settings in enterprise accounts:

| Action             | Description      |
|--------------------|------------------|
| `globalcatalog-collection.enterprise-settings.read` | An event is generated when you view the enterprise settings. |
| `globalcatalog-collection.enterprise-settings.update` | An event is generated when you update the enterprise settings. |
| `globalcatalog-collection.enterprise-settings.list` | An event is generated when you get a list of the enterprises in an account and their corresponding settings. |
{: caption="Actions that generate events for managing catalog settings in enterprise accounts" caption-side="bottom"}

## Events for managing software licenses and entitlements
{: #at_actions_manage_license}

The following table lists the actions that generate events for managing software licenses and entitlements:

| Action             | Description      |
|--------------------|------------------|
| `entitlement.entitlement.create`       | An event is generated when an initiator binds a license to an account. |
| `entitlement.entitlement.delete`       | An event is generated when an initiator deletes an entitlement. |
| `entitlement.entitlement.delete_purge` | An event is generated when an initiator purges an entitlement. |
| `entitlement.entitlement.update`       | An event is generated when an initiator updates an entitlement. |
| `entitlement.entitlement.check`        | An event is generated when an initiator uses an entitlement to pull an image from the governed IBM Container Registry. |
| `entitlement.entitlement.invalidate`   | An event is generated when an entitlement's license is not valid anymore. |
{: caption="Actions that generate events for managing software licenses and entitlements" caption-side="bottom"}

## Events for managing software instances
{: #at_events_sw_instance}

The following table lists the actions that generate an event for software instances:

| Action                                           | Description                                                           |
|--------------------------------------------------|-----------------------------------------------------------------------|
| `globalcatalog-instance.offering-instance.create` | An event is generated when you create a software instance. |
| `globalcatalog-instance.offering-instance.delete` | An event is generated when you delete a software instance. |
| `globalcatalog-instance.offering-instance.list` | An event is generated when you list all software instances in an account. |
| `globalcatalog-instance.offering-instance.read` | An event is generated when you retrieve a software instance. |
| `globalcatalog-instance.offering-instance.retrieve_history` | An event is generated when you access the audit logs for a software instance. |
| `globalcatalog-instance.offering-instance.update` | An event is generated when you install updates to a software instance. |
| `globalcatalog-instance.dashboard.view` | An event is generated when you access the software instance details page. |
{: caption="Actions that generate events for software instances" caption-side="top"}

## Analyzing catalog management activity tracking events
{: #at_events_cm_analyze}



You can find the value `unavailable` in catalog events. This value indicates when an update is made, but specific details about the update aren't included.
{: important}
