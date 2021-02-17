---

copyright:
  years: 2021
lastupdated: "2021-02-17"

keywords: troubleshoot permission to attach and detach access management tags

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

# Why can't I attach or detach access management tags on a resource?
{: #troubleshoot-attach-detach-accesstag}
{: troubleshoot}

If you can't attach or detach access management tags on a resource, you might need to check the following items:
* List of the existing tags
* The type of access you're assigned
* Type of the resource
{: shortdesc}

You can't attach or detach access management tags on a resource, which you have access to.
{: tsSymptoms}
   
This problem can be commonly caused by the following reasons:
{: tsCauses}
* You're trying to attach an access management tag that doesn't exist yet in the account, which you are a member of. You need to [create the access management tag](https://{DomainName}/account/tags) first.
* You might not be assigned the appropriate access to complete the actions. You must have the Administrator role on the resource.
* The resource is not an IAM-enabled resource. Only a set of {{site.data.keyword.Bluemix}} services is enabled to use {{site.data.keyword.Bluemix}} IAM for access control. These services need to be labeled as "IAM-enabled" in the catalog.
* Some services don't have full support for access management tags on their UI, so when you're creating an instance of those services, you can only attach user tags. To learn how you can work with access management tags, see the tutorial about [controlling access to resources by using tags](/docs/account?topic=account-access-tags-tutorial).

Complete the following steps to check your level of access. If you need to request access, contact the account owner.
{: tsResolve}

Go to **Manage** > **Access (IAM)** in the console, and select your name on the **Users** page.

* To see IAM access policies that are assigned to you, select the **Access policies**. 
* To determine what access you have through the access groups you are assigned, select **Access groups** and check the access policies on the access groups.

To view the allowed actions for each role that has been assigned to you, click **Actions for role**.
{: tip}
