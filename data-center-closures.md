---

copyright:

  years: 2020, 2025
lastupdated: "2025-02-12"

keywords: data centers, data center support, datacenter, data center closure

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Data center migrations
{: #dc-closure}

As part of the data center modernization strategy for {{site.data.keyword.cloud}}, a data center is scheduled to consolidate.
{: shortdesc}

{{site.data.keyword.cloud_notm}} invests significantly in data center infrastructure. These investments include rolling out newer data centers and multizone regions (MZRs) designed to deliver a more resilient architecture with higher levels of network throughput and redundancy. For more information, see [Locations for resource deployment](/docs/overview?topic=overview-locations).

Part of this modernization strategy is to consolidate select data centers. As this transition approaches, help is available to assist you in your migration to modern data centers. For more information, see [Migrating resources to a different data center](/docs/account?topic=account-migrate-data-center) or [FAQ for migrating resources to a different data center](/docs/account?topic=account-faqs-migrating-resources).

The following table shows the location with the associated data center that is set to close, and the recommended data centers to which you can migrate.

| Location | Data Center to Close |  Recommended Data Centers | Migration Deadline |
|----------|----------------------|---------------------------|--------------------|
| Milan    | MIL01                | Frankfurt, Madrid, London, Amsterdam, or any WW IBM Cloud data center | 10 December 2025 |
| Dallas   | DAL09: POD3 and POD4 | DAL10, DAL12, DAL13       | 4 March 2025       |
{: caption="Data center that is closing in 2025" caption-side="top"}

The following table describes important dates that you need to be aware of if you have services that run in the DAL09 data center. You receive notifications if you have services in the data center that is closing.

| Date             | Data Center Migration Milestone |
|------------------|---------------------------------|
| 06 August 2024   | Official announcements for all impacted customers in DAL09 - POD3 and POD4 datacenter |
| 06 August 2024   | No new account provisioning in impacted datacenter. |
| 14 October 2024  | Last date to provision services in impacted datacenter. |
| 05 February 2025 | Network maintenance DAL09 - POD3 and POD4. 10:AM US Eastern Time (14:00 GMT). Remaining services in DAL09 PODs 3 and 4 will experience network disruption during the network maintenance. Customers will need to contact IBM Cloud to restore service. |
| 10 February 2025 | Last date to submit migration assistance request. |
| 04 March 2025    | Last date to migrate before consolidation of DAL09 - POD3 and POD4 datacenter begins. |
{: caption="Timeline for DAL09 data center migration" caption-side="top"}


The following table describes important dates that you need to be aware of if you have services that run in the MIL01 data center. You receive notifications if you have services in the data center that is closing.

| Date             | Data Center Migration Milestone |
|------------------|---------------------------------|
| 07 January 2025   | Official Announcement for all impacted customers in MIL01 datacenter. |
| 07 January 2025   | No New Account provisioning in impacted datacenter. |
| 10 June 2025  | Last date to provision services in impacted datacenter. |
| 09 September 2025 | Network maintenance MIL01: 10:AM US Eastern Time (14:00 GMT). Remaining services in MIL01 will experience network disruption during the network maintenance. Customers will need to contact IBM Cloud to restore service. |
| 10 November 2025 | Last date to submit migration assistance request. |
| 10 December 2025    | Last date to migrate before closure of MIL01 datacenter. |
{: caption="Timeline for MIL01 data center migration" caption-side="top"}
