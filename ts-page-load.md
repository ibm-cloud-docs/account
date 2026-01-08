---

copyright:

  years: 2015, 2026
lastupdated: "2026-01-08"

keywords: troubleshoot account, page load, page error, console page error

subcollection: account

content-type: troubleshoot

---

{{site.data.keyword.attribute-definition-list}}

# Why do I encounter console pages that don't load?
{: #ts_err}
{: troubleshoot}

A page in the {{site.data.keyword.Bluemix}} console might not load properly, and an error message is displayed.
{: shortdesc}

One of the following error messages might be displayed:
{: tsSymptoms}

```text
BXNUI0001E: The page wasn't loaded because IBM Cloud didn't detect whether a session exists.
BXNUI0016E: The apps and services weren't retrieved because an IBM Cloud page didn't load.
500 internal server error
```

An issue with the browser is causing a console page to not load. Or, there might be a temporary issue with connectivity.
{: tsCauses}

Complete one or more of the following actions, as necessary:
{: tsResolve}

* Refresh or restart your browser.
* Log out of the console and log in again.
* Use the private browsing mode of your browser.
* Clear the cookies and the cache of the browser.
* Use a different browser. For the list of supported browsers, see [{{site.data.keyword.cloud_notm}} prerequisites](/docs/overview?topic=overview-prereqs-platform).
* If the problem persists, go to the [{{site.data.keyword.cloud_notm}} Status page](https://cloud.ibm.com/status){: external} to check if a service or component has an issue.
