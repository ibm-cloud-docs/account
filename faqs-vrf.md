---

copyright:

  years: 2023, 2026
lastupdated: "2026-10-23"

keywords: account settings, delete account, account errors, vrf account migration, account migration, vrf, classic account

subcollection: account

content-type: faq

---

{{site.data.keyword.attribute-definition-list}}

# FAQ for {{site.data.keyword.cloud}} classic account VRF migration
{: #vrf-faqs}

Find answers to frequently asked questions about IBM Cloud classic account migration to VRF-style accounts, including automatic conversion and network connectivity.
{: shortdesc}

By default, classic accounts established before 30 November 2023 are included in the IBM Cloud general routing table. Beginning 30 November 2023, any new or empty classic account without provisioned VLANs is automatically converted to a VRF-style account the next time it initiates a private network connection. To find all FAQ for {{site.data.keyword.cloud_notm}}, see our [FAQ library](/docs/faqs).

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

## Can customers enable VRF on their account?
{: #permissions-enable-VRF}
{: faq}

Yes. An account owner can enable VRF on an account by enabling VRF and service endpoints. For more information on how to enable VRF on an account, see [Enabling VRF and service endpoints](/docs/account?topic=account-vrf-service-endpoint&interface=ui).

## What permissions are required for a user to enable VRF on their account?
{: #permissions-enable-account-VRF}
{: faq}

No specific permissions are required for an account user to enable VRF. However, certain conditions like, the account must not have IPSec VPN configured, custom spanning must be disabled, and the account must not already be using VRF must be met. For more information on how to enable VRF on an account, see [Enabling VRF and service endpoints](/docs/account?topic=account-vrf-service-endpoint&interface=ui).

## What permissions are required for a user to enable service endpoint on their account?
{: enable-serviceendpoint}
{: faq}

The account owner has the privilege to enable or disable service endpoints. Other users must have the `MANAGE_PRIVATE_ENDPOINT_SERVICE` privilege to perform these actions. Also, the account must enable a VRF beforehand. For more information on how to enable service endpoints on an account, see [Enabling service endpoints](/docs/account?topic=account-vrf-service-endpoint&interface=ui#service-endpoint).
