---

copyright:
  years: 2015, 2021
lastupdated: "2021-02-25"

keywords: troubleshoot account, account problem, runtime memory allowance, exceed runtime allowance
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

# How did I exceed the runtime memory allowance?
{: #noruntimemem}
{: troubleshoot}

You went over the allowed memory for your {{site.data.keyword.Bluemix}} account.
{: shortdesc}

You're unable to deploy apps, and an error states that you've exceeded your organization's memory limit.
{: tsSymptoms}

In a Lite account, your Cloud Foundry apps can use up to 256 MB of instantaneous runtime memory. In billable accounts, there's a 2 GB memory limit.
{: tsCauses}

If you're using a Lite account, you can get more memory by upgrading to a billable account. Go to **Manage > Account** in the {{site.data.keyword.Bluemix_notm}} console, and select **Account settings**. For more information about Lite account features, see [Lite account](/docs/account?topic=account-accounts#liteaccount).
{: tsResolve}

If you don't want to upgrade from a Lite account but have some idle apps, you can delete them to free up some runtime memory.