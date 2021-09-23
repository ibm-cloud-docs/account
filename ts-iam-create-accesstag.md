---

copyright:
  years: 2021
lastupdated: "2021-09-22"

keywords: troubleshoot permission to create access management tags

subcollection: account

content-type: troubleshoot

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

# Why can't I create access management tags?
{: #troubleshoot-create-accesstag}
{: troubleshoot}

If you can't create an access management tag within an {{site.data.keyword.Bluemix}} account that you're not the owner of, you might need to check the type of access you're assigned.
{: shortdesc}

You can't create access management tags in an account of which you are a member. 
{: tsSymptoms}

This problem can commonly occur by one of the following reasons:
{: tsCauses}

* You might not be assigned the appropriate access to complete the action. You must have the Administrator role on the Tagging Service that is listed under the Account management services or Administrator role on all Account management services.
* You reached the limit of 30 access management tags per account.
* Some services don't have full support for access management tags on their UI, so when you're creating an instance of those services, you can only attach user tags. To learn how you can work with access management tags, see the tutorial about [controlling access to resources by using tags](/docs/account?topic=account-access-tags-tutorial).

Complete the following steps to check your level of access. If you need to request access, contact the account owner.
{: tsResolve}

Go to **Manage** > **Access (IAM)** in the console, and select your name on the **Users** page. 

1. To view the IAM access policies that are assigned to you, click **Access policies**. 
2. To view the policies that are included in an access group that you might be assigned to, click **Access groups** > **access_group_name** > **Access policies**.

To view the allowed actions for each role that has been assigned to you, click **Actions for role**.
{: tip}
