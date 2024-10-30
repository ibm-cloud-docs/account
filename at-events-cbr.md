---

copyright:
  years: 2024
lastupdated: "2024-10-30"

keywords: activity tracking, context-based restrictions events, events, observibility

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}




# Activity tracking events for context-based restrictions
{: #at_events_cbr}



{{site.data.keyword.cloud_notm}} context-based restrictions generate activity tracking events.
{: shortdesc}

Activity tracking events report on activities that change the state of a service in {{site.data.keyword.cloud_notm}}. You can use the events to investigate abnormal activity and critical actions and to comply with regulatory audit requirements.

You can use {{site.data.keyword.atracker_full_notm}}, a platform service, to route auditing events in your account to destinations of your choice by configuring targets and routes that define where activity tracking events are sent. For more information, see [About {{site.data.keyword.atracker_full_notm}}](/docs/atracker?topic=atracker-about).

You can use {{site.data.keyword.logs_full_notm}} to visualize and alert on events that are generated in your account and routed by {{site.data.keyword.atracker_full_notm}} to an {{site.data.keyword.logs_full_notm}} instance.



As of 28 March 2024, the {{site.data.keyword.at_full_notm}} service is deprecated and will no longer be supported as of 30 March 2025. Customers will need to migrate to {{site.data.keyword.logs_full_notm}} before 30 March 2025. During the migration period, customers can use {{site.data.keyword.at_full_notm}} along with {{site.data.keyword.logs_full_notm}}. Activity tracking events are the same for both services. For information about migrating from {{site.data.keyword.at_full_notm}} to {{site.data.keyword.logs_full_notm}} and running the services in parallel, see [migration planning](/docs/cloud-logs?topic=cloud-logs-migration-intro).
{: important}

## Locations where activity tracking events are sent to {{site.data.keyword.at_full_notm}} hosted event search
{: #at-legacy-locations}

[Deprecated]{: tag-red}



Context-based restrictions sends activity tracking events to {{site.data.keyword.at_full_notm}} hosted event search in the regions that are indicated in the following table.

| Dallas (`us-south`) | Washington (`us-east`)  | Toronto (`ca-tor`) | Sao Paulo (`br-sao`) |
|---------------------|-------------------------|-------------------|----------------------|
| [No]{: tag-red} | [No]{: tag-red} | [No]{: tag-red} | [No]{: tag-red} |
{: caption="Regions where activity tracking events are sent in Americas locations" caption-side="top"}
{: #at-table-1}
{: tab-title="Americas"}
{: tab-group="at"}
{: class="simple-tab-table"}
{: row-headers}

| Tokyo (`jp-tok`)    | Sydney (`au-syd`) |  Osaka (`jp-osa`) | Chennai (`in-che`) |
|---------------------|------------------|------------------|--------------------|
| [No]{: tag-red} | [No]{: tag-red} | [No]{: tag-red} | [No]{: tag-red} |
{: caption="Regions where activity tracking events are sent in Asia Pacific locations" caption-side="top"}
{: #at-table-2}
{: tab-title="Asia Pacific"}
{: tab-group="at"}
{: class="simple-tab-table"}
{: row-headers}

| Frankfurt (`eu-de`)  | London (`eu-gb`) | Madrid (`eu-es`) |
|---------------------------------------------------------------|---------------------|------------------|
| [Yes]{: tag-green} | [No]{: tag-red} | [No]{: tag-red} |
{: caption="Regions where activity tracking events are sent in Europe locations" caption-side="top"}
{: #at-table-3}
{: tab-title="Europe"}
{: tab-group="at"}
{: class="simple-tab-table"}
{: row-headers}

Events are available in the `Frankfurt (eu-de)` region.

To view these events, you must provision an instance of the [IBM Cloud Activity Tracker](/docs/activity-tracker?topic=activity-tracker-provision#provision) service [Deprecated]{: tag-red} in the Frankfurt (eu-de) region. Then, you must open the [IBM Cloud Activity Tracker UI](/docs/activity-tracker?topic=activity-tracker-launch).

## Locations where activity tracking events are sent by {{site.data.keyword.atracker_full_notm}}
{: #atracker-locations}



The context-based restrictions service sends activity tracking events by {{site.data.keyword.atracker_full_notm}} in the regions that are indicated in the following table.

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

### Enabling activity tracking events for context-based restrictions
{: #at-enable-cbr}






The context-based restrictions service generates [global activity tracking events](/docs/atracker?topic=atracker-event_types#event_types_global) for the actions that are listed in this document. To track and log those events for auditing in your account, complete the following steps:

1. Create an instance of {{site.data.keyword.logs_full_notm}}.
   1. Click the **Navigation Menu** icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Observability** to access the *Observability* dashboard.
   1. Click **Logging > Instances > Cloud Logs > Create**.
   1. Select the `Frankfurt (eu-de)` region for high availability.
   1. Accept the terms and click **Create**.

1. Create an Activity Tracker target.
   1. Go to **Observability > Activity Tracker > Routing > Targets**.
   1. Click **Create**.
   1. Select the {{site.data.keyword.logs_full_notm}} instance that you created in the `Frankfurt (eu-de)`.
   1. Click **Create target**.

1. Create an Activity Tracker route.
   1. Go to **Observability > Activity Tracker > Routing > Routes**.
   1. Click **Create**.
   1. Select `Platform events (global)` as the location to send audit events from.
   1. Select the target {{site.data.keyword.logs_full_notm}} instance that you created in the `Frankfurt (eu-de)` region.

1. Create {{site.data.keyword.cos_full_notm}} buckets in the `Frankfurt (eu-de)` region.
   - A [data bucket](/docs/cloud-logs?topic=cloud-logs-configure-data-bucket)
   - A [metrics bucket](/docs/cloud-logs?topic=cloud-logs-configure-metrics-bucket&interface=cli)

   The same bucket cannot be used as both your data bucket and your metrics bucket.
   {: note}

1. Connect your storage buckets to your {{site.data.keyword.logs_full_notm}} instance.
   1. Go to **Observability > Logging > Instances** and select your {{site.data.keyword.logs_full_notm}} instance.
   1. Click **Storage**
   1. For **Logs data**, click **Connect**.
      1. Click **Authorize now** to allow {{site.data.keyword.logs_full_notm}} and {{site.data.keyword.cos_full_notm}} to connect.

      You can view the authorization policy that this creates on the [Authorizations](/iam/authorizations){: external} page.
      {: note}

      1. Select the logs bucket that you created.
      1. Click **Connect**.
   1. For **Events to metrics data**, click **Connect**.
      1. Click **Authorize now** to allow {{site.data.keyword.logs_full_notm}} and {{site.data.keyword.cos_full_notm}} to connect.
      1. Select the metrics bucket that you created.
      1. Click **Connect**.

### Launching {{site.data.keyword.logs_full_notm}} from the Observability page
{: #log-launch-standalone-cbr}



For information on launching the {{site.data.keyword.logs_full_notm}} UI, see [Launching the UI in the {{site.data.keyword.logs_full_notm}}.](/docs/cloud-logs?topic=cloud-logs-instance-launch)

### Viewing activity tracking events for context-based restrictions
{: #at-viewing-cbr}



You can use {{site.data.keyword.logs_full_notm}} to visualize and alert on events that are generated in your account and routed by {{site.data.keyword.atracker_full_notm}} to an {{site.data.keyword.logs_full_notm}} instance.

To view context-based restrictions events in the {{site.data.keyword.logs_full_notm}} dashboard, go to the **Subsystems** filter and select the value `context-based restrictions`.

## Network zone events
{: #network_zone_events}

The following table lists the actions that generate nerwork zone events:

| Action | Description |
| -----  | ----------- |
| context-based-restrictions.zone.create | An event is generated when an initiator creates a CBR zone. |
| context-based-restrictions.zone.list | An event is generated when an initiator lists CBR zones. |
| context-based-restrictions.zone.read | An event is generated when an initiator looks at information that is related with a CBR zone. |
| context-based-restrictions.zone.update | An event is generated when an initiator modifies a CBR zone. Users can identify system initiated updates (vs. user initiated updates) by the initiator name "IBM". |
| context-based-restrictions.zone.delete | An event is generated when an initiator deletes a CBR zone. |
{: caption="Events that are generated for network zone events" caption-side="top"}


## Context-based restrictions rules events
{: #restriction_rules_events}

The following table lists the actions that generate context-based restricitons rule events:

| Action | Description |
| -----  | ----------- |
| context-based-restrictions.policy.create | An event is generated when an initiator creates a CBR rule. |
| context-based-restrictions.policy.list | An event is generated when an initiator lists CBR rules. |
| context-based-restrictions.policy.read | An event is generated when an initiator looks at information that is related with a CBR rule. |
| context-based-restrictions.policy.update | An event is generated when an initiator modifies a CBR rule. |
| context-based-restrictions.policy.delete | An event is generated when an initiator deletes a CBR rule. |
{: caption="Events that are generated for context-based restrictions rules" caption-side="top"}


## Account settings events
{: #account_setting_events}

The following table lists the actions that generate account settings events:

| Action | Description |
| -----  | ----------- |
| context-based-restrictions.account-settings.read | An event is generated when an initiator looks at information that is related with account settings. |
{: caption="Events that are generated for context-based restrictions account settings events" caption-side="top"}


## Analyzing context-based restrictions activity tracking events
{: #at_events_cbr_analyze}



For more informatino, see [Monitoring context-based restrictions](/docs/account?topic=account-cbr-monitor).
