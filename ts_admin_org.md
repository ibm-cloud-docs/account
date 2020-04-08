---

copyright:
  years: 2015, 2020
lastupdated: "2020-04-08"

keywords: troubleshoot account, account problem, view all orgs 
subcollection: account
---

{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:new_window: target="_blank"}
{:troubleshoot: data-hd-content-type='troubleshoot'}

# Why can't administrators use the console to view all orgs?
{: #ts_ui_org}
{: troubleshoot}

As an administrator, you can't display every organization to administer them when you use the {{site.data.keyword.Bluemix_notm}} console. You can display and administer only those organizations to which you belong.

As an administrator, you can't view all the organizations from the console.
{: tsSymptoms}

This behavior is a limitation of the console.
{: tsCauses}

You can use commands such as `ibmcloud account orgs` and `ibmcloud account org-create` from the {{site.data.keyword.Bluemix_notm}} command-line interface to manage all the organizations. For a full list of commands, enter `ibmcloud account help`.
{: tsResolve}