---

copyright:
  years: 2021
lastupdated: "2021-09-28"

keywords: troubleshoot accessing all instances of a service

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

# Why can't a user in my account access all instances of a service?
{: #troubleshoot-instances}
{: troubleshoot}

If a user in your account can't access all instances of a service, you might need to check the type of access they're assigned.
{: shortdesc}

A user has an access policy on a specific service in the account, but they can't access all instances.
{: tsSymptoms}
   
The access policy might not be set up correctly. This problem can be commonly caused by the following reasons:
{: tsCauses}

* The user is not in the expected access group.
* The assigned role to the user is not correct.
* The service is not using the correct access management tag. The tag in your IAM policy must be the same tag that is attached to the instances of the service.

Complete the following steps to check the level of access of the user.
{: tsResolve}

Go to **Manage** &gt; **Access (IAM)** in the console, and select the user's name on the **Users** page.

* To see IAM access policies that are assigned to them, select the **Access policies**. 
* To determine what access they have through the access groups they are assigned, select **Access groups** and check the access policies on the access groups.

To view the allowed actions for each role that has been assigned to them, click **Actions for role**.
{: tip}

Make sure that the service is using the correct access management tag on your [resource list](/account/tags).
