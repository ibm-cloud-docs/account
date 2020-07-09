---

copyright:

  years: 2017, 2020

lastupdated: "2020-06-09"

keywords: users level of access, user control, access control, permissions, manage access, access management, platform management tasks, assign roles

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}

# Access management in {{site.data.keyword.Bluemix_notm}}
{: #cloudaccess}

Access management enables you to control which users see, create, use, and manage resources in your account. To grant access, you can assign roles that allow users levels of access for completing platform management tasks and accessing account resources.
{: shortdesc}

The way that you manage access in {{site.data.keyword.Bluemix}} depends on the type of resource that you want to assign access to. {{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM) is the access management system that is used for consistently managing resources that are organized in a resource group across the {{site.data.keyword.Bluemix_notm}} platform. Classic infrastructure and Cloud Foundry resources are not managed by using Cloud IAM. These resource types have their own access management systems. 

If you have a combination of resource types, you manage each type separately:

* For [IAM resources](/docs/account?topic=account-userroles), go to **Manage** &gt; **Access (IAM)** in the console, and then select **Users**, **Access groups**, or **Service IDs** to get started.
* For assigning access to your [classic infrastructure resources](/docs/account?topic=account-infrapermission), you set permissions within **Manage** > **Access (IAM)** on the Classic infrastructure tab for the user that you want to assign access. 
* For assigning access to [Cloud Foundry resources](/docs/account?topic=account-cfaccess), you assign users to orgs and set Cloud Foundry org and space access roles within **Manage** > **Access (IAM)** on the Cloud Foundry tab for the user.

While each type of access is managed separately, all access policies are made up of a subject you want to assign access to, a target for the policy to scope what the subject has access to, and then finally an IAM role, Cloud Foundry role, or classic infrastructure permission to determine the level of access the subject has on the target.

![Access management policies by using IAM, Cloud Foundry, or classic infrastructure permissions.](images/access-management.svg "How assigning policies works by starting with a subject, selecting a target, then assigning a role or permission"){: caption="Figure 1. Access management policies by using IAM, Cloud Foundry, or classic infrastructure permissions" caption-side="bottom"}

For IAM policies, the subject can be an access group, user, or service ID. And, the target can be an account management service, resource group, service in the account, specific service instance, or resource type within a service. Platform and service roles can be selected to scope the level of access for the subject. For Cloud Foundry access, a user is given access to a Cloud Foundry org and space by selecting each and assigning an org role and space role. For classic infrastructure, a user is selected, and then the access can be scoped to a service or device with specific permissions assigned.


