---

copyright:

  years: 2021, 2022

lastupdated: "2022-12-27"

keywords: troubleshooting services, troubleshooting resources, service problems, resource problems, resource group, reactivate resource, upgrade resource, reactiveate account, upgrade account

subcollection: account

content-type: troubleshoot

---

{{site.data.keyword.attribute-definition-list}}

# Why can't I reactivate or upgrade a suspended account?
{: #resource_inactive}
{: troubleshoot}

When you try to reactivate or upgrade a closed Lite account, the process does not complete successfully.
{: shortdesc}

The following error message displays when you try to create a new service instance:
{: tsSymptoms}

> The resource group `<name>` is inactive with state: `SUSPENDED`

This is a known issue and limitation for deactivated accounts. At the discretion of IBM, accounts that violate the acceptable usage behavior of the {{site.data.keyword.cloud}} services can be deactivated without notice. Some services can be restored if users correct their usage behaviors after they're notified of the offensive action. For more information, see [Acceptable Internet use policy for IBM services](https://www.ibm.com/services/us/imc/html/aup1.html){: external}.
{: tsCauses}

To resolve the issue, [create a support case](/docs/get-support?topic=get-support-open-case) and include the group name from the error message in the case details.
{: tsResolve}
