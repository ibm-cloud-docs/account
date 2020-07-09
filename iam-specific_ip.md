---

copyright:

  years: 2018, 2020

lastupdated: "2020-04-16"

keywords: specific IP addresses, IP addresses, restrict IP access, IP address access, allow IP access

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}

# Allowing specific IP addresses for a user
{: #ips}

By default, all IP addresses can be used to log in to the {{site.data.keyword.cloud}} console and access classic infrastructure APIs. You can specify which IP addresses have access, and only the specified addresses are allowed can be used and all others are restricted.
{:shortdesc}

If you have the following assigned access, you can update the restricted IP addresses for another user:

  * An IAM policy with the Editor or higher role on the User management service.
  * You are an ancestor in the classic infrastructure hierarchy for the user and you have the Manage users classic infrastructure permission assigned

If you have the User-managed login setting that is enabled on your User details page, you can manage this setting for yourself.
{: tip}

To restrict a user to using only specific IP addresses, complete the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, click **Manage** &gt; **Access (IAM)**, and select **Users**.
2. Select a user from the list.
3. From the User details page, go to the **IP address restrictions** section.
4. For **Cloud platform**, enter the IP addresses. The IP addresses listed are the only ones from which this user can log in to {{site.data.keyword.Bluemix}}.
5. For **Classic infrastructure**, enter the IP addresses. The IP addresses listed are the only ones from which the user can call a classic infrastructure API.

  To enter a classic infrastructure IP address, the user must already have a classic infrastructure API key created.
  {: note}
