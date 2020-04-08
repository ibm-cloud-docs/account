---

copyright:
  years: 2015, 2020
lastupdated: "2020-04-08"

keywords: troubleshoot enterprise, enterprise problem, import enterprise, existing enterprise

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

# Why can't I import an existing account to the enterprise?
{: #troubleshoot-existing-enterprise}
{: troubleshoot}

To import an existing enterprise, you must have the correct access roles assigned on the billing service. 

When you try to import an existing account to enterprise, one of the following issues occurs:
{: tsSymptoms}
* When you click **Add existing account** in the Account section, the account that you want to add is not listed.
* You don't have the option to click **Import account**.

You aren't assigned the correct access, or the account isn't eligible to be imported.
{: tsCauses}

If you can't see the existing account that you want to import, you need the Administrator role on the Billing service of the existing account.
{: tsResolve}

If the **Import account** option isn't available, verify that you have the Administrator or Editor role on the Billing service of the enterprise and the Administrator or Editor role on the Enterprise service for the parent enterprise or account group.

If the account that you want to import is a Pay-As-You-Go account and you're still unable to import it after you verify you have access, the account might not be eligible to be imported into the enterprise. Some Pay-As-You-Go accounts can't be directly imported into an enterprise, such as many Pay-As-You-Go accounts that are billed in United States dollars (USD). Contact [{{site.data.keyword.Bluemix_notm}} Sales](https://cloud.ibm.com/catalog?contactmodule){: new_window} ![External link icon](../icons/launch-glyph.svg) to convert the account to a Subscription account, and then import it into the enterprise.
