---

copyright:
  years: 2020, 2022
lastupdated: "2022-11-29"

keywords: account known issues, catalog known issues, catalog management, private catalogs, catalogs, IBM Cloud catalog, IAM, maximum limits for creating IAM resources, delete users from account, context-based restrictions

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}


# Known issues and limitations
{: #known-issues}

Known issues and limitations include not being able to restrict access to some products in the {{site.data.keyword.cloud}} catalog, the maximum limits for creating {{site.data.keyword.cloud_notm}} Identity and Access Management (IAM) resources, and not being able to delete users from accounts that have too many Cloud Foundry orgs.
{: shortdesc}


## Catalog management settings don't apply to some {{site.data.keyword.IBM_notm}} products
{: #settings-noapply}

Some products are not affected by the following catalog visibility settings:

- Turning off the the visibility of the {{site.data.keyword.Bluemix_notm}} catalog
- Excluding all {{site.data.keyword.Bluemix_notm}} products from the catalog
- Excluding all {{site.data.keyword.Bluemix_notm}} products from your private catalogs

You can view and manage catalog visibility settings by going to **Manage > Catalogs > Settings** in the {{site.data.keyword.Bluemix_notm}} console.
{: note}

Users can still create instances of the following products by using an API or the CLI, regardless of the catalog visibility setting in the account or private catalog:

* {{site.data.keyword.block_storage_is_short}}
* {{site.data.keyword.vpx_full}}
* Fortigate Security Appliance
* Hardware Firewall
* Hardware Firewall Dedicated
* {{site.data.keyword.backup_notm}}
* {{site.data.keyword.cloud_notm}} {{site.data.keyword.baremetal_short}}
* {{site.data.keyword.cloud_notm}} {{site.data.keyword.blockstorageshort}}
* {{site.data.keyword.registrylong_notm}}
* {{site.data.keyword.cloud_notm}} Content Delivery Network
* {{site.data.keyword.cloud_notm}} Direct Link
* {{site.data.keyword.cloud_notm}} Direct Link on Classic
* {{site.data.keyword.IBM_notm}} {{site.data.keyword.openwhisk_short}}
* {{site.data.keyword.cloud_notm}} Gateway Appliance
* {{site.data.keyword.cloud_notm}} Hardware Security Modules
* {{site.data.keyword.containerlong_notm}}
* {{site.data.keyword.cos_full_notm}}
* {{site.data.keyword.bplong_notm}}
* {{site.data.keyword.cloud_notm}} Load Balancer
* {{site.data.keyword.cloud_notm}} {{site.data.keyword.BluVirtServers_short}}
* Subnets and IPs
* Virtual Private Cloud
* Virtual Server for VPC
* VLANs
* VPN
* VPN for VPC

## {{site.data.keyword.Bluemix_notm}} IAM limits
{: #iam_limits}

The following table lists the maximum limits for IAM resources. These limits apply to any user who can create IAM resources. If a limit is exceeded, you receive an exception and are not allowed to create any new resources beyond that limit.

If you have a specific use case that requires an extended limit, you can request an increase. For more information, see [Increasing account limits](/docs/account?topic=account-account-limits).
{: note}

| Resource                               | Max  |
|----------------------------------------|------|
| Access groups per account              | 500  |
| Access groups per user                 | 50   |
| Access management tags per account     | 250   |
| API Keys per identity                  | 20   |
| Cloud Foundry orgs                     | 500  |
| Custom roles per account               | 40   |
| Dynamic rules per access group         | 100  |
| Dynamic rules per trusted profile      | 20   |
| Dynamic rules per Identity provider (IdP) | 2000 |
| IdPs per account  | 5    |
| Policies per account [^tabletext]      | 4020 |
| Policies per subject within an account | 1000  |
| Policies with access management tags within an account   | 25   |
| Service IDs per account                | 2000 |
| Trusted profiles per account           | 2000 |
| Users per trial account                | 100  |
| Users per billable account             | 7500 |
{: caption="Table 1. IAM account limits" caption-side="top"}

[^tabletext]: IAM policies and context-based restrictions rules share a combined limit of 4020.

A maximum of 1,000 policies and service to service authorizations within one account is recommended to ensure optimal performance within your account. For more information about limiting the number of policies in your account, see the [Best practices for organizing resources and assigning access](/docs/account?topic=account-account_setup).
{: tip}

If you want to check the number of policies in your account, see [Viewing the total number of policies per account](/docs/account?topic=account-account-limits&interface=cli#total-number-policies-cli). To request an increase in the account limit, see [Requesting a policy and rule shared limit increase](/docs/account?topic=account-account-limits&interface=cli#limit-increase).

### Policy limitations based on attributes
{: #access-tag-limits}

Access management tags are only available when you create an access policy that is scoped for all IAM-enabled services. In this case, when you enable the access based on tags, no other attributes can be added. And, when you base your policy on a specific location or resource group, no tag can be added to the access policy.

### Trusted profile limitations
{: #tp-limits}

Users can't use the Support Center when they log in to {{site.data.keyword.cloud_notm}} by applying a trusted profile.

## Context-based restrictions limits

The following table lists the maximum limits for context-based restrictions. These limits apply to any user who can create context-based restrictions rules or network zones. For more information, see [What are context-based restrictions?](/docs/account?topic=account-context-restrictions-whatis).

If you have a specific use case that requires an extended limit, you can request an increase. For more information, see [Increasing account limits](/docs/account?topic=account-account-limits).
{: note}

| Resource                               | Max  |
|----------------------------------------|------|
| Context-based restriction rules per account [^tabletext2] | 4020 |
| Network zones per account              | 500 |
| IP addresses per network zone              | 1000 |
| IP addresses per rule             | 1000 |
{: caption="Table 2. Context-based restrictions limits" caption-side="top"}

[^tabletext2]: IAM policies and context-based restrictions rules share a combined limit of 4020.

A context-based restriction rule that includes multiple network zones can have a maximum of 1000 IP addresses indirectly associated with it. For example, in a rule that includes two network zones, one of the zones could have 800 IP addresses and the other could have a maximum of 200 IP addresses.
{: note}

If you want to check the number of rules in your account, see [Viewing the total number of rules per account](/docs/account?topic=account-account-limits&interface=cli#total-number-rules-cli). To request an increase in the account limit, see [Requesting a policy and rule shared limit increase](/docs/account?topic=account-account-limits&interface=cli#limit-increase).

### Eventual consistency
{: #cbr-eventual-consistency}

Context-based restrictions follow an [eventually consistent](https://en.wikipedia.org/wiki/Eventual_consistency){: external} pattern that is common to many cloud-native services. As a result, Context-based restrictions remain highly available and performant across multiple global regions. Changes that are made to Context-based restrictions rules and network zones are recorded and propagated worldwide. Access changes might not take effect until the propagation process is complete, usually within a few minutes.
