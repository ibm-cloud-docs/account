---

copyright:
  years: 2021, 2022

lastupdated: "2022-06-20"

keywords: frequently asked questions, cbr faqs, cbr and iam, context-based restrictions, access restrictions

subcollection: account

content-type: faq

---

{{site.data.keyword.attribute-definition-list}}

# FAQs about Context-based restrictions
{: #cbrfaq}

FAQs for {{site.data.keyword.cloud}} Context-based restrictions might include questions about access restrictions for {{site.data.keyword.cloud_notm}} resources. 
{: shortdesc}

To find all FAQs for {{site.data.keyword.cloud}}, see our [FAQ library](/docs/faqs).

## What are {{site.data.keyword.cloud_notm}} Context-based restrictions?
{: #whatiscbr}
{: faq}
{: support}

As an account owner or administrator, you can define and enforce access restrictions for {{site.data.keyword.cloud}} resources based on the network location of access requests by enabling context-based restrictions. For more information, see [What are context-based restrictions?](/docs/account?topic=account-context-restrictions-whatis).

## How do you use Context-based restrictions and IAM policies together?
{: #iam-cbr-diff}
{: faq}

These restrictions work with traditional IAM policies, which are based on identity, to provide an extra layer of protection. Since both IAM access and context-based restrictions enforce access, context-based restrictions offer protection even in the face of compromised or mismanaged credentials.

Unlike IAM policies, context-based restrictions don't assign access. Context-based restrictions check that an access request comes from an allowed context that you configure. 
{: note}

## What's the difference between Context-based restrictions and allowed IP addresses?
{: #ip-cbr-diff}
{: faq}

 Context-based restrictions enforce access restrictions at the individual service level and access is evaluated when a user attempts to access a resource. Allowed IP address restrict access at the account level, which is evaluated at login.
