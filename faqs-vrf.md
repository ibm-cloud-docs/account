---

copyright:

  years: 2023, 2025
lastupdated: "2025-04-14"

keywords: account settings, delete account, account errors, vrf account migration, account migration, vrf, classic account

subcollection: account

content-type: faq

---

{{site.data.keyword.attribute-definition-list}}

# FAQ about VRF account migration
{: #vrf-faqs}

By default, classic accounts that were established before 30 November 2023, are included in the {{site.data.keyword.cloud}} general routing table. Previously, if you wanted to convert a classic account to a VRF-style account, you were required to open a support case with {{site.data.keyword.IBM}} Support. Beginning 30 November 2023, any new classic account or any existing classic account that is "empty" (for example, without any provisioned VLANs), will be automatically converted to a VRF-style account the next time that account initiates a private network connection. To find all FAQ for {{site.data.keyword.cloud_notm}}, see our [FAQ library](/docs/faqs).
{: shortdesc}

## Will this affect current accounts that currently have existing servers or other Private Network connections?
{: #existing-account}
{: faq}

No. This change affects only newly created classic accounts or existing "empty" accounts that have no private network connections (for example, no private VLANs, servers, or other private network connectivity).

## Are there any products that are incompatible with a VRF-style account?
{: #incompatible-vrf}
{: faq}

Classic IPsec VPNs are incompatible with VRF-style accounts. After an account is migrated to a VRF-style account, you cannot order classic IPsec VPNs going forward.

If you require an IPSec VPN, you must order either a gateway appliance or a regular bare metal or virtual server with VPN software to facilitate the connection. In addition, classic SSL VPNs are no longer globally routed. This means that you must connect through a VPN into the specific data center endpoint that you want to reach.

## I can no longer do VLAN spanning. Is this expected behavior?
{: #vlan-spanning}
{: faq}

Yes. After you migrate to a VRF-style account, the option to turn VLAN Spanning "off" is not available.

By default, in a VRF-style account, all subnets and VLANs on the account can communicate with each other. If you need subnet/VLAN segregation, you must order a gateway appliance (one for each POD, where necessary) to appropriately block traffic.
