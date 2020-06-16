---

copyright:
  years: 2015, 2020
lastupdated: "2020-04-08"

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
{:new_window: target="_blank"}
{:troubleshoot: data-hd-content-type='troubleshoot'}

# Why do I encounter console pages that don't load?
{: #ts_err}
{: troubleshoot}

When you use the {{site.data.keyword.Bluemix_notm}} console, you might not be able to load a console page. Instead, error messages BXNUI0001E or BXNUI0016E might be displayed.

One of the following error messages might be displayed:
{: tsSymptoms}

`BXNUI0001E: The page wasn't loaded because {{site.data.keyword.Bluemix_notm}} didn't detect whether a session exists.`

`BXNUI0016E: The apps and services weren't retrieved because an {{site.data.keyword.Bluemix_notm}} page didn't load.`

An issue with the browser is causing a console page to not load.
{: tsCauses}

Complete one or more of the following actions, as necessary:
{: tsResolve}

  * Refresh or restart your browser.
  * Log out of {{site.data.keyword.Bluemix_notm}} and log in again.
  * Use the private browsing mode of your browser.
  * Clear the cookies and the cache of the browser.
  * Use a different browser. For more information about browsers that are supported by {{site.data.keyword.Bluemix_notm}}, see [{{site.data.keyword.Bluemix_notm}} prerequisites](/docs/overview?topic=overview-prereqs-platform).
  * If you installed the Cloud Foundry command-line interface, enter the `ibmcloud cf apps` command to see whether your app is running.
