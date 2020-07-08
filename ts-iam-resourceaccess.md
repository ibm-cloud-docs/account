---

copyright:
  years: 2020
lastupdated: "2020-06-09"

keywords: troubleshoot access to a resource, why can't user access resource

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

# Why can't a user I gave access work with a resource from the Resource list page?
{: #troubleshoot-serviceaccess}
{: troubleshoot}

Users in your account must have access to the service or service instance and the containing resource group to access the instance from the Resource list page.
{: shortdesc}

A user has an access policy on a specific resource or a service in the account, but they can't access the service from the Resource list page.

When the user selects the service name, the following error message is displayed:
{: tsSymptoms}

`You do not have access to any organizations, spaces, or resource groups in this region. Check that you have the appropriate access with your account owner or administrator.`
   
In addition to access to the type of service or specific resource, the user must also be assigned access to the resource group or space that contains the resource. To access the resource instance within a specific account, a user must be assigned at least the Viewer role or higher on the resource group itself. 
{: tsCauses}

1. In the {{site.data.keyword.cloud_notm}} console, go to **Manage** &gt; **Access (IAM)**, and select the user's name from **Users** page. 
1. From the row for the user that you want to assign access, select the **Actions** ![List of actions icon](../icons/action-menu-icon.svg) menu, and click **Assign access**.
1. Select **Assign users additional access**.
1. Select the **IAM services** tile. 
1. Select the type of access you want to assign, then select a specific resource group if you want to limit the user to view or manage only resources in that resource group, or select **All resource groups**. 
1. Next, select the role that you want the user to have. The Viewer role is sufficient to enable the user to access the resource. 
1. Click **Add** to add the access to the access summary. 
1. Click **Assign**. 
{: tsResolve}


