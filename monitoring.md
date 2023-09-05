---

copyright:
  years: 2018, 2023
lastupdated: "2023-09-05"

keywords: manage account, account events, track events, account tracking, monitoring, catalog tracking, catalog management

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Auditing events for account, IAM, catalog management
{: #acct_iam_tracking}

As a security officer, auditor, or manager, you can use the {{site.data.keyword.at_full}} service to track how users and applications interact with an {{site.data.keyword.Bluemix}} account, the {{site.data.keyword.Bluemix_notm}} catalog, private catalogs, and with {{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM).
{: shortdesc}

To get started with monitoring your user's actions, see [{{site.data.keyword.at_short}}](/docs/activity-tracker?topic=activity-tracker-getting-started#getting-started).

## Account management events
{: #account-management-events}

You can track the following events:

* Managing an account by creating an account, updating information, activating an account, or creating a Subscription account
* Adding or removing users
* Creating organizations

## IAM events
{: #tracking-iam}

You must create an instance of the {{site.data.keyword.at_short}} service in the `Frankfurt (eu-de)` region to start tracking IAM events. When you create the instance, you can track the following events:

* Managing access groups by creating and deleting groups or adding and removing users
* Creating, updating, or deleting service IDs
* Creating, updating, or deleting API keys
* Creating, updating, or deleting access policies
* Creating, updating, or deleting trusted profiles
* Logging in to {{site.data.keyword.Bluemix_notm}} by using an API key, authorization code, passcode, password, or an API key associated with a service ID
* Logging in to {{site.data.keyword.Bluemix_notm}} by using a trusted profile. For more information, see [Monitoring login sessions for trusted profiles](/docs/account?topic=account-trusted-profile-monitor).

For more information, see [IAM events](/docs/activity-tracker?topic=activity-tracker-at_events_iam).

### Enterprise IAM events
{: #enterprise-iam-events}

In addition, you can track the following events in an enterprise account:
* Creating, updating, or deleting enterprise-managed IAM templates
* Assigning enterprise-managed IAM templates to child accounts

You can track the following enterprise events in a child account:
* Enterprise-managed IAM templates assigned to your account

For more information, see [IAM events](/docs/activity-tracker?topic=activity-tracker-at_events_iam).

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

For more information, see [Account management events](/docs/activity-tracker?topic=activity-tracker-at_events_acc_mgt).

## Context-based restrictions events
{: #cbr-events}

You can track the following events:

* Creating, updating, or deleting rules
* Creating, updating, or deleting network zones

For more information, see [Context-based restrictions events](/docs/activity-tracker?topic=activity-tracker-auditing-events-for-context-based-restrictions).
