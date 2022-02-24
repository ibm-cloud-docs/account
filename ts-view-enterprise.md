---

copyright:
  years: 2015, 2022
lastupdated: "2022-02-21"

keywords: troubleshoot enterprise, enterprise problem, can't view enterprise, access to enterprise

subcollection: account

content-type: troubleshoot
---

{{site.data.keyword.attribute-definition-list}}


# Why can't I view the entire enterprise?
{: #troubleshoot-view-enterprise}
{: troubleshoot}

If you aren't able to view the entire {{site.data.keyword.Bluemix}} enterprise, you might need to check what access you are assigned.
{: shortdesc}

You can view a few of the accounts in the enterprise but not the entire enterprise hierarchy. The account hierarchy shows only accounts that you have access to, not the entire enterprise account.
{: tsSymptoms}

You are assigned access to only certain accounts in the enterprise.
{: tsCauses}

To check what access you are assigned, complete the following steps:
{: tsResolve}

1. Go to **Manage** &gt; **Access (IAM)** > **Users** in the {{site.data.keyword.Bluemix_notm}} console.
2. Select your name.
3. Click the **Access policies** tab.

Contact the enterprise owner to request the correct access.

If you're the owner of the enterprise, complete the following steps to assign a user access to the entire enterprise:
1. Go to **Manage** > **Access (IAM)** > **Users** in the {{site.data.keyword.cloud_notm}} console.
2. Select the name of the user.
3. Click the **Access policies** tab > **Assign access** > **Assign access to account management services**.
4. Select **Enterprise** as the service, and select the name of your enterprise.
5. Select the account group or account in the enterprise that you want to give the user access to. For example, if you want a user to have access to view only a single account, select the account and assign the user the Viewer role or higher. If you want a user to have access to view the entire enterprise, leave the account group and account selections blank, and assign the access.
