---

copyright:
  years: 2020, 2021
lastupdated: "2021-02-25"


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

You must have specific access to invite users to an {{site.data.keyword.Bluemix}} account if you aren't the account owner.
{: shortdesc}

If you are not the account owner and aren't assigned the correct access, then you can't invite users to an account. 

You can't invite users to the account.
{: tsSymptoms}
   
You might not be assigned the correct access. 
{: tsCauses}

To invite users and manage outstanding invitations, you must be an account owner, an organization manager, a user with an IAM access policy with Editor or higher role on the user management account management service, or you must have classic infrastructure permissions to add users.
{: tsResolve}

After you have the correct access, go to **Manage > Access (IAM)**, then select **Users**, and click **Invite users** to add users to the account.
