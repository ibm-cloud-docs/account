---

copyright:
  years: 2015, 2025
lastupdated: "2025-11-15"

keywords: troubleshoot account, account problem, lite plan, lite plan instance, extra instance, create instance

subcollection: account

content-type: troubleshoot

---

{{site.data.keyword.attribute-definition-list}}

# Why can't I create a new Lite plan instance?
{: #nosecondlite}
{: troubleshoot}

You try to create more than one instance in your Lite account.
{: shortdesc}

You receive the following error message when you try to create a new Lite plan instance:
{: tsSymptoms}

```text
Unable to provision new Lite instance
The account already has an instance created with the Lite plan
```

There's a limit of one instance per Lite plan to help ensure that these plans stay free. For more information about Lite account features, see [Lite account](/docs/account?topic=account-accounts#liteaccount).
{: tsCauses}

You can create more instances of the service by selecting one of the billable service plans, which are available in the billable accounts. To upgrade to a billable account from the console, go to **Manage** > **Account** in the {{site.data.keyword.cloud_notm}} console, and select **Account settings**.
{: tsResolve}

If you don't want to upgrade from a Lite account and are no longer using your existing Lite service instance, you can delete the existing Lite plan instance from the dashboard and then create a new instance. When you delete the Lite plan instance, all the data that is associated with that instance is deleted and isn't recoverable.
