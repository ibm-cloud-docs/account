---

copyright:

  years: 2021, 2025
lastupdated: "2025-01-28"

keywords: troubleshooting services, troubleshooting resources, service problems, resource problems, resource group, reactivate resource, upgrade resource, reactiveate account, upgrade account

subcollection: account

content-type: troubleshoot

---

{{site.data.keyword.attribute-definition-list}}

# Why does a resource group error occur after reactivation or upgrade of a suspended account?
{: #resource_inactive}
{: troubleshoot}

When you try to reactivate or upgrade a closed Lite account, the process does not complete successfully.
{: shortdesc}

The following error message displays when you try to create a new service instance:
{: tsSymptoms}

> The resource group `<name>` is inactive with state: `SUSPENDED`

Or when you view the list of resource groups for the account, you no longer have a group named Default.

This is a known issue and limitation for deactivated accounts that have been restored. At the discretion of IBM, accounts that violate the acceptable usage behavior of the {{site.data.keyword.cloud}} services can be deactivated without notice. Some services can be restored if users correct their usage behaviors after they're notified of the offensive action. For more information, see [Acceptable Internet use policy for IBM services](https://www.ibm.com/services/us/imc/html/aup1.html){: external}.
{: tsCauses}

To resolve the issue, [create a support case](/docs/account?topic=account-open-case) and include the group name from the error message in the case details.
{: tsResolve}

 
