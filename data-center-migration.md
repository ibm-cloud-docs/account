---

copyright:

  years: 2020, 2025
lastupdated: "2025-08-09"

keywords: migrate, migrating data center, migrate resources, data center

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Migrating resources to a different data center
{: #migrate-data-center}

{{site.data.keyword.IBM}} continually updates and modernizes data centers to give you higher levels of performance. Some data centers aren't able to be upgraded, so they must be closed and you must migrate your resources to a different data center.
{: shortdesc}

Throughout the data center migration process, help is available. To take advantage of special offers, or learn about recommended configurations, use one of the following options to contact the {{site.data.keyword.IBM_notm}} 24x7 Client Success team:

* [Live chat](https://www.ibm.com/solutions/cloud-data-centers){: external}
* Phone: (US) 866-597-9687; (EMEA) +31 20 308 0540; (APAC) +65 6622 2231

For information about which data centers are closing, see [Data center closures](/docs/account?topic=account-dc-closure). For a list of the data centers that are available, see [Locations for resource deployment](/docs/overview?topic=overview-locations).

## Migrating your resources
{: #migrating-your-resources}

Complete the following steps to migrate resources to a new data center:

1. Identify any virtual server instances or bare metal servers that are currently running on the data centers that are set to close.
   1. Begin by [viewing all subnets](/docs/subnets?topic=subnets-view-all-subnets).
   1. [Filter the list of subnets](/docs/subnets?topic=subnets-view-all-subnets#filter-details) by location, such as `Dallas 5`.
   1. In the resulting filtered list, click the name of the VLAN in the **VLAN** column. To identify a specific POD within a data center, check the VLAN name for a string like, `bcr02` or `fcr04`. `Bcr02` = backend customer router, POD 2. `Fcr04` = frontend customer router, POD 4.
   1. On the **Instance detail** page, locate the **Devices** section that identifies virtual server instances and bare metal servers that are provisioned in the VLAN.
   1. To identify all devices in the data center, complete these steps for each VLAN in the data center.

1. Order replacement servers in new data centers. For more information, see the following documentation:

* [Planning for VPC instances](/docs/vpc?topic=vpc-vsi_best_practices)
* [Getting started with virtual servers](/docs/virtual-servers?topic=virtual-servers-getting-started-tutorial)
* [Getting started with bare metal servers](/docs/bare-metal?topic=bare-metal-getting-started)
* [Comparing {{site.data.keyword.cloud_notm}} Classic and VPC infrastructure environments](/docs/infrastructure-hub?topic=infrastructure-hub-compare-infrastructure)

1. Copy your data to a new server by using the following methods. You must establish connectivity between the old and new servers and have sufficient storage in the new server.

* Use [Secure Copy Protocol (SCP)](https://www.ibm.com/docs/en/flashsystem-v7000u){: external} to securely copy a file from source to destination.
* Use [rsync](https://download.samba.org/pub/rsync/rsync.1){: external} if you need to copy multiple files. Rsync also copies directory structures and preserves file permissions.
* Migrate your virtual server instance [from one classic data center to another](/docs/virtual-servers?account=virtual-servers-migrating-vsi-new-datacenter).
* Migrate your [virtual server instance](/docs/vpc?topic=vpc-migrate-vsi-to-vpc) by creating an image template and deploying it in a new {{site.data.keyword.vpc_short}}.
* Migrate your [VMware cluster](/docs/vmwaresolutions?topic=vmwaresolutions-hcxclient-migrations) to a new data center by using HCX.
* Migrate a local load balancer to [IBM Cloud Load Balancer](/docs/loadbalancer-service?topic=loadbalancer-service-getting-started). For more information, see [FAQ for IBM Cloud Load Balancer](/docs/loadbalancer-service?topic=loadbalancer-service-faqs-for-ibm-cloud-load-balancer).
* Migrate your [{{site.data.keyword.cos_full_notm}}](/docs/cloud-object-storage?topic=cloud-object-storage-migrate-data-center#migrating-your-resources) data to a new {{site.data.keyword.cloud_notm}} data center.

Copy only applications and application data between systems. Copying older versions of operating system files to a newer version can cause problems. Shut down databases before you copy them between the systems to ensure that the data is consistent. When migrating database data, migrate the data in a way that doesn’t limit your options to import it into the new system. Rather than copying database data from system to system, consider exporting it to a format so you can import it to a newer database. Flat text files, CSV files, and other files provide more options than using proprietary or closed file formats when it comes to moving data between systems. Always test your data migration approaches on a limited set of test data before officially copying.

1. Cancel your servers. You continue to be invoiced for the old servers until you cancel them. For more information, see [Device types](/docs/virtual-servers?topic=virtual-servers-managing-virtual-servers#device-types-and-actions).
