---

copyright:
  years: 2018, 2020
lastupdated: "2020-06-03"

keywords: manage account, account events, track events, account tracking, monitoring, catalog tracking, catalog management

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:external: target="_blank" .external}
{:tip: .tip}
{:deprecated: .deprecated}

# Auditing events for account, IAM, catalog management
{: #acct_iam_tracking}

As a security officer, auditor, or manager, you can use the {{site.data.keyword.at_full}} service to track how users and applications interact with an {{site.data.keyword.Bluemix}} account, the {{site.data.keyword.Bluemix_notm}} catalog, private catalogs, and with {{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM).
{:shortdesc}

As of 9 May 2019 the {{site.data.keyword.cloudaccesstraillong}} service is deprecated. You must create an instance of the {{site.data.keyword.at_short}} in your account to continue tracking account management and IAM events. For more information, see [Deprecation of the IBM Cloud Activity Tracker service](https://www.ibm.com/cloud/blog/release-notes/deprecating-ibm-cloud-activity-tracker){: external}.
{: deprecated}


## Account management events
{: #account-management-events}

You can track the following events:

* Managing an account by creating an account, updating information, activating an account, or creating a Subscription account
* Adding or removing users
* Creating organizations

## IAM events
{: #tracking-iam}

You must create an instance of the {{site.data.keyword.at_short}} service in the `eu-de` region to start tracking IAM events. When you create the instance, you can track the following events:

* Managing access groups by creating and deleting groups or adding and removing users
* Creating, updating, or deleting service IDs
* Creating, updating, or deleting API keys
* Creating, updating, or deleting access policies
* Logging in to {{site.data.keyword.Bluemix_notm}} by using an API key, authorization code, passcode, password, or an API key associated with a service ID

To get started monitoring your user's actions, see [{{site.data.keyword.at_short}}](/docs/Activity-Tracker-with-LogDNA?topic=Activity-Tracker-with-LogDNA-getting-started#getting-started). For more information about each of the event areas that you can track, see [IAM events](/docs/Activity-Tracker-with-LogDNA?topic=Activity-Tracker-with-LogDNA-at_events_iam).

## Catalog management events
{: #catalog-management-events}

You can track the following events:

* Viewing or updating account settings
* Viewing or updating a catalog
* Listing all products in a catalog
* Listing all products in an account
* Creating, updating, viewing, or deleting a product

`unavailable` indicates when an update is made, but specific details about the update aren't included. 
{: important}

For more information about each of the event areas that you can track, see [Account management events](/docs/Activity-Tracker-with-LogDNA?topic=Activity-Tracker-with-LogDNA-at_events_acc_mgt).