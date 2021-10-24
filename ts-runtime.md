---

copyright:
  years: 2015, 2021
lastupdated: "2021-10-25"

keywords: troubleshoot account, account problem, runtime memory allowance, exceed runtime allowance
subcollection: account

content-type: troubleshoot

---

{{site.data.keyword.attribute-definition-list}}

# How did I exceed the runtime memory allowance?
{: #noruntimemem}
{: troubleshoot}

You went over the allowed memory for your {{site.data.keyword.Bluemix}} account.
{: shortdesc}

You're unable to deploy apps, and an error states that you've exceeded your organization's memory limit.
{: tsSymptoms}

In Lite accounts that were created before 12 August 2021, your Cloud Foundry apps can use up to 256 MB of instantaneous runtime memory. In Pay-As-You-Go or Subscription accounts, there's a 2 GB memory limit.
{: tsCauses}

You can get more memory by upgrading your Lite account. Go to **Manage** > **Account** in the {{site.data.keyword.Bluemix_notm}} console, and select **Account settings**. For more information about Lite account features, see [Lite account](/docs/account?topic=account-accounts#liteaccount).
{: tsResolve}

If you don't want to upgrade from a Lite account but have some idle apps, you can delete them to free up some runtime memory.
