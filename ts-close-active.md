---

copyright:
  years: 2025
lastupdated: "2025-10-24"

keywords: cancel active resources, close account

subcollection: account

content-type: troubleshoot

---

{{site.data.keyword.attribute-definition-list}}

# Why can't I close my account after canceling all services?
{: #troubleshoot-account-close}
{: troubleshoot}
{: support} 

You are unable to close your account because you receive an error indicating that the account has active resources even though the Resource list page is empty.
{: shortdesc}

When you click **Close account** in the account settings, an error message states that you have active resources even though no resources appear in the Resource list. You followed the steps in [Closing an account](/docs/account?topic=account-account-close) to cancel all services, devices, and billing items.
{: tsSymptoms}

This issue can occur when a floating IP address that is associated with a resource remains active because floating IPs are not displayed in the Resource list.
{: tsCauses}

Check for a floating IP address, and then remove or disassociate it from the resource. Find the floating IP address on the **Infrastructure > Network > Floating IPs** page, click its overflow menu (**...**), and click **Unassociate**.
{: tsResolve}

See also [Considerations when deleting a VPC](/docs/vpc?topic=vpc-deleting) if the account you are trying to close had VPC resources.
