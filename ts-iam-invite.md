---

copyright:
  years: 2020. 2022
lastupdated: "2021-02-21"


keywords: troubleshoot invite users, access to invite users, access to add users

subcollection: account

content-type: troubleshoot

---

{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:codeblock: .codeblock}
{:pre: .pre}
{:note:.deprecated}
{:troubleshoot: data-hd-content-type='troubleshoot'}

# How can I get access to invite users to the account? 
{: #troubleshoot-invite}
{: troubleshoot}

You must have specific access to invite users to an {{site.data.keyword.Bluemix}} account if you aren't the account owner. Without the correct access, you can't invite users to an account. 
{: shortdesc}

When you click **Invite users**, the following message might be displayed:
{: tsSymptoms}

`Looks like you don't have access to invite users. You must be assigned the editor or administrator role for the User management service or be a Cloud Foundry org manager. Contact your account owner for access.`

You aren't assigned the correct access. 
{: tsCauses}

To invite users and manage outstanding invitations, you must be an account owner, an organization manager, a user with an IAM access policy with the Editor role or higher on the user management account management service, or you must have classic infrastructure permissions to add users. 
{: tsResolve}

To review your assigned access in the account, complete the following steps: 

1. In the {{site.data.keyword.cloud_notm}} console, click **Manage** > **Access (IAM)**, and select **Users**. 
2. Select your name. 
3. Review the assigned access in the **Access policies** section.

If you aren't assigned the correct access, contact the account owner. After you have the correct access, go to **Manage > Access (IAM)**, then select **Users**, and click **Invite users** to add users to the account.

If you're the account owner and can't invite users, contact [Support](/unifiedsupport/supportcenter){: external}.

To contact support, you can use the following methods:
* If you have a Pay-As-You-Go or Subscription account, you can click **Live chat with support**.
* Pay-As-You-Go or Subscription accounts can also contact support by phone: +1-866-403-7638.
* You can [create a case](/unifiedsupport/cases/form){: external}. 
