---

copyright:
  years: 2015, 2020
lastupdated: "2020-11-18"

keywords: troubleshoot account, page load, page error, console page error

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
{:troubleshoot: data-hd-content-type='troubleshoot'}

# Why do I encounter console pages that don't load?
{: #ts_err}
{: troubleshoot}

A page in the {{site.data.keyword.Bluemix}} console might not load properly, and an error message is displayed. 
{: .shortdesc}

One of the following error messages might be displayed:
{: tsSymptoms}

`BXNUI0001E: The page wasn't loaded because {{site.data.keyword.Bluemix_notm}} didn't detect whether a session exists.`

`BXNUI0016E: The apps and services weren't retrieved because an {{site.data.keyword.Bluemix_notm}} page didn't load.`

`500 internal server error`

An issue with the browser is causing a console page to not load. Or, there might be a temporary issue with connectivity.
{: tsCauses}

Complete one or more of the following actions, as necessary:
{: tsResolve}

  * Refresh or restart your browser.
  * Log out of the console and log in again.
  * Use the private browsing mode of your browser.
  * Clear the cookies and the cache of the browser.
  * Use a different browser. For more information about browsers that are supported by {{site.data.keyword.Bluemix_notm}}, see [{{site.data.keyword.Bluemix_notm}} prerequisites](/docs/overview?topic=overview-prereqs-platform).
  * If you installed the Cloud Foundry CLI, enter the `ibmcloud cf apps` command to see whether your app is running.
  * Try again later.
  * If the problem persists, go to the [{{site.data.keyword.Bluemix_notm}} Status page](https://cloud.ibm.com/status){: external} to check whether a service or component has an issue.
