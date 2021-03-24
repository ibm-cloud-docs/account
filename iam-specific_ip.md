---

copyright:

  years: 2018, 2021

lastupdated: "2021-03-24"

keywords: specific IP addresses, IP addresses, restrict IP access, IP address access, allow IP access

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}

# Allowing specific IP addresses 
{: #ips}

By default, all IP addresses can be used to log in to the {{site.data.keyword.cloud}} console and access classic infrastructure APIs. You can specify which IP addresses have access and all other IP addresses are restricted. You can specify this access at the user level or at the account level. 
{:shortdesc}

If an IP address restriction is defined for both the account and the user, the IP address needs to match both specifications to be able to generate an IAM token.
{: important}

## Allowing specific IP addresses for a user
{: #ips_user}

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
  
  You can enter a single IP address `192.168.0.0`, an IP address range `192.168.0.1 - 192.168.2.53`, or IP subnets               `192.168.0.0/16`. Make sure to use IPv4 or IPv6 addresses, and to separate multiple values with a comma. 
  {: note}
  
1. Click **Save**. 

  To enter a classic infrastructure IP address, the user must have already created a classic infrastructure API key.
  {: note}

## Allowing specific IP addresses for an account 
{: #ips_account}

If you have the following assigned access, you can update the restricted IP addresses for an account:

  * An IAM policy with the Editor, Operator, or Administrator role on the IAM identity service.

To restrict all users to using only specific IP addresses, complete the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, click **Manage** &gt; **Access (IAM)**, and select **Settings**.
1. From the Account restrictions section, turn on the **IP address access** setting. 
1. Enter the IP addresses. The IP addresses listed are the only ones from which users in the account can log in to {{site.data.keyword.Bluemix}}.
  
  You can enter a single IP address `192.168.0.0`, an IP address range `192.168.0.1 - 192.168.2.53`, or IP subnets `192.168.0.0/16`. Make sure to use IPv4 or IPv6 addresses, and to separate multiple values with a comma. 
  {: note}
  
1. Click **Save**. 

