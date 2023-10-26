---

copyright:
  years: 2015, 2023
lastupdated: "2023-10-24"

keywords: account settings, delete account, account errors, reassign account, view tags, batch registration, transfer account ownership

subcollection: account

content-type: faq

---

{{site.data.keyword.attribute-definition-list}}

# FAQs about VRF account migration
{: #vrf-faqs}

By default, classic accounts established prior to November 30, 2023 are included in the IBM Cloud general routing table. Previously, if you wanted to convert a classic account to a VRF-style account you were required to open a support case with IBM Support. Beginning November 30, 2023, any new Classic account, or any existing Classic account that is "empty" (for example, without any provisioned VLANs), will be automatically converted to a VRF-style account the next time that account initiates a private network connection. 
{: shortdesc}

## Will this affect current accounts that currently have existing servers or other Private Network connections?
{: #existing-account}
{: faq}

No, this will only affect newly-created Classic accounts, or existing "empty" accounts that have no private network connections (for example, no private VLANs, servers, or other private network connectivity).

## Are there any products incompatible with a VRF-style account?
{: #incompatible-vrf}
{: faq}

Classic IPSec VPNs are incompatible with VRF-style accounts. Once an account migrates to a VRF-style account, you will be unable to order classic IPSec VPNs going forward. 

If you require an IPSec VPN, you will need to order either a Gateway Appliance or a regular bare metal or virtual server with VPN software to facilitate the connection. In addition, Classic SSL VPNs will no longer be globally routed. This means you must connect through a VPN into the specific datacenter endpoint that you wish to reach.

## I can no longer VLAN spanning. Is this expected behavior?
{: #vlan-spanning}
{: faq}

Yes, after migrating to a VRF-style account, the option to turn VLAN Spanning "off" will no longer be available. 

By default, in a VRF-style account, all subnets and VLANs on the account can communicate with each other. If you need subnet/VLAN segregation, you will need to order a Gateway Appliance (one for each POD where necessary) to appropriately block traffic.
