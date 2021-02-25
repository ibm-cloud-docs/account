---

copyright:
  years: 2015, 2021
lastupdated: "2021-02-25"

keywords: troubleshoot enterprise, enterprise problem, enterprise subscriptions, enterprise permissions, enterprise access

subcollection: account

content-type: troubleshoot
---

{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:troubleshoot: data-hd-content-type='troubleshoot'}

# Why can't I see the enterprise subscriptions?
{: #troubleshoot-viewsub-enterprise}
{: troubleshoot}

You can't see the Subscriptions page content in the console due to lack of access.
{: shortdesc}

When you go to view the Subscriptions page in the {{site.data.keyword.Bluemix}} console from a child account, the following message is displayed:
{: tsSymptoms}

`Looks like you don't have permission to view subscription data for this account. Contact your account owner or administrator to request access.`

The following message is displayed in the Billing section on your enterprise dashboard:

`Looks like you don't have permission to view this information. Learn more about IAM access.`

Access to billing and payment information for future billing periods is restricted to users in the enterprise account. Users in a child account can't access billing and payment information, such as subscriptions, even if they previously had access in the account.
{: tsCauses}

To view or manage billing, you need to be invited to the enterprise account and given access to the Billing service in that account. Contact the account owner to request access.
{: tsResolve}
