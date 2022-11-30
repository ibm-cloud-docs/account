---

copyright:
  years: 2015, 2021
lastupdated: "2021-09-22"

keywords: troubleshoot account, account problem, spaces in an org, create app
subcollection: account

content-type: troubleshoot
---

{{site.data.keyword.attribute-definition-list}}


# Why are no spaces associated with my current org?
{: #ts_no_space}
{: troubleshoot}

You can't create an app if no space is associated with your current organization.
{: shortdesc}

When you try to create an app the following error message is displayed:
{: tsSymptoms}

`BXNUI0097E: Before you can add an app, at least one space must be associated with your organization and region. On the Dashboard, click Create a Space. When the space is created, try again.`

Apps must be created in a space under your organization.
{: tsCauses}

To create a space, use one of the following methods:
{: tsResolve}

* From the console menu bar, click **Manage > Account**. Expand **Account resources** and click **Cloud Foundry orgs**. Then, select the organization in which you want to create the space, and click **Add a space**.
* From the {{site.data.keyword.Bluemix_notm}} CLI, enter `ibmcloud account space-create <space_name> -o <organization_name>`.
