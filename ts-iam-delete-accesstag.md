---

copyright:
  years: 2021
lastupdated: "2021-09-28"

keywords: troubleshoot permission to delete access management tags

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

# Why can't I delete access management tags?
{: #troubleshoot-delete-accesstag}
{: troubleshoot}

If you can't delete an access management tag within an {{site.data.keyword.Bluemix}} account that you're not the owner of, you might need to check the type of access you're assigned. Or, the tag might be attached to a resource.
{: shortdesc}

* You can't delete access management tags in an account of which you are a member.
* You have the permission, but still unable to delete an access management tag.
{: tsSymptoms}

The action might be blocked by one of the following reasons:
{: tsCauses}

* You might not be assigned the appropriate access to complete the action. You must have the Administrator role on the Tagging Service that is listed under the Account management services or Administrator role on all Account management services.
* The access management tag you're trying to delete is still attached to an active or a reclaimed resource.

Complete the following steps to check your level of access. If you need to request access, contact the account owner.
{: tsResolve}

Go to **Manage** > **Access (IAM)** in the console, and select your name on the **Users** page. 

1. To view the IAM access policies that are assigned to you, click **Access policies**. 
2. To view the policies that are included in an access group that you might be assigned to, click **Access groups** > **access_group_name** > **Access policies**.

To view the allowed actions for each role that has been assigned to you, click **Actions for role**.
{: tip}

Before you try to delete an access management tag, make sure it's not attached to any of your resources.
* Filter by tag name on your [resource list](/account/tags). If you don't have a viewer permission for all existing resources, contact the account owner to verify.
* Use the **`ibmcloud resource reclamation`** command in the {{site.data.keyword.Bluemix}} CLI to list out resources in reclamation state and delete the resource that had the tag you were trying to delete. For more information, see [Using resource reclamations](/docs/account?topic=account-resource-reclamation).

When you delete an access management tag from the account, any associated IAM policies are also deleted with it.
{: note}
