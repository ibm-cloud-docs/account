---

copyright:
  years: 2015, 2021
lastupdated: "2021-06-14"

keywords: troubleshoot account, account problem, add user to org, org, invite user to org
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
{:external: target="_blank" .external}
{:troubleshoot: data-hd-content-type='troubleshoot'}

# Why can't I add users to an org?
{: #ts_adduser}
{: troubleshoot}

You can invite users to your organization only if you're the account owner, or if you're both a manager and a member of the organization.
{: shortdesc}

You can't see the **Invite a New User** link in your **Manage Organizations** section.
{: tsSymptoms}

Only the following {{site.data.keyword.Bluemix_notm}} users can invite users to an organization:
{: tsCauses}
  * The account owner of the organization
  * Organization managers who are also members, not collaborators, of the organization

In {{site.data.keyword.Bluemix_notm}}, you can be either a member or a collaborator of an organization:

<dl><dt>Collaborator</dt>
<dd>You are a collaborator of an organization if you already have an {{site.data.keyword.Bluemix_notm}} account, and someone else invites you to the organization.</dd>
<dt>Member</dt>
<dd>You are a member of an organization if you don't have an {{site.data.keyword.Bluemix_notm}} account, but then someone invites you to the organization and you sign up for {{site.data.keyword.Bluemix_notm}} from the invitation.</dd>
</dl>

You can't invite users to your organization if you're a collaborator of the organization, even if you're assigned as an organization manager.

All organization managers, including collaborators in an organization, can add, modify, and remove users that are already in the organization.
{: note}

If you can't invite users to your organization and need a different role to do so, contact your organization manager to change your role. To identify your organization manager, complete the following steps:
{: tsResolve}

  1. From the console menu bar, click **Manage** > **Account**, and select **Company contacts**.
  2. Go to your organization, and view the information of organization manager on the **USERS** tab.  

If you can't invite users because you're a collaborator and not a member, you must delete your previous {{site.data.keyword.Bluemix_notm}} account and then be invited to join the account as a member of the organization. To delete your previous account and join the account as a member, complete the following steps:

  1. Contact [{{site.data.keyword.Bluemix_notm}} Support](https://cloud.ibm.com/unifiedsupport/supportcenter){: external} to open a support case and request to delete your account. If you have data that is associated with your old account that you want to save and move to the new account, include this information in your email.
  2. After your account is deleted, have a user with the organization manager role invite you to the organization as an organization manager. Then, sign up for {{site.data.keyword.Bluemix_notm}} from the invitation.
  
