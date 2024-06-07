---

copyright:
  years: 2020, 2022
lastupdated: "2022-12-21"

keywords: troubleshoot create service, create service error

subcollection: account

content-type: troubleshoot

---

{{site.data.keyword.attribute-definition-list}}

# Why can’t I create a new service instance?
{: #ts_create_service}
{: troubleshoot}

You are unable to create or add a new service instance.
{: shortdesc}

You might receive one of the following error messages when you create a service:
{: tsSymptoms}

> Create service error.

or

> Create Service [500, Internal Server Error]. An error occurred while trying to create the service. Please try again later.

Creating a service instance can fail when you don't have access, exceed a plan limit, or experience a problem with your web browser. An active incident or planned maintenance might also affect your ability to create a service instance.
{: tsCauses}

To resolve this issue, use one of the following methods:
{: tsResolve}

* You might not have the correct access. You must have the editor role or higher to create a service instance. Contact the account owner to request the correct access. For more information, see [Cloud IAM roles](/docs/account?topic=account-userroles#iamusermanrol).

* Creating an instance might exceed a plan or account limit. Review the plan features on the catalog page or in the specific service's documentation. From the Resource list page, you can view what instances currently exist that count towards the plan or account limit. For example, there's a limit of one instance per Lite plan.

* If you're experiencing a web browser issue, see [Why do I encounter console pages that don't load?](/docs/account?topic=account-ts_err).

* Go to the [{{site.data.keyword.Bluemix_notm}} - Status](https://cloud.ibm.com/status){: external} page to check if an active incident or planned maintenance is affecting your ability to create a service instance.
