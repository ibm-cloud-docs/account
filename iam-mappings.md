---

copyright:

  years: 2022, 2023

lastupdated: "2023-09-05"

keywords: IAM, what is IAM, comparing IAM concepts

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Mapping {{site.data.keyword.cloud_notm}} IAM concepts to other cloud providers
{: #iam-compare}

Identity and access management is used to securely authenticate users and provide access to cloud resources. While IAM across cloud providers is a consistent way of securing authentication and access, the concepts within each cloud provider and how they apply might differ. Review the following information in the table to learn more about how concepts in {{site.data.keyword.cloud_notm}} IAM relate or compare to those of other cloud providers to help you onboard smoothly with {{site.data.keyword.cloud_notm}}.

## Comparing IAM concepts
{: #compare-concepts}

The following mappings of {{site.data.keyword.cloud_notm}} IAM concepts to those of other cloud providers, such as Amazon Web Services (AWS), Google Cloud Platform, and Microsoft Azure, might not be an exact one-to-one match. However, if you are familiar with a particular concept within another provider, this mapping is intended to help you find the closest related concept in {{site.data.keyword.cloud_notm}}.


|  {{site.data.keyword.cloud_notm}} concept | {{site.data.keyword.cloud_notm}} description  | AWS   | Azure | Google Cloud Platform  |
|-----------|----------------|-------|-------|------------------------|
| Identities  | Users and service IDs |  Users, groups, and roles | User, group, service principal, managed identity | User accounts and service accounts. Supported identity types: Google Account, Service account, Google group, G Suite domain, Cloud Identity domain |
| Users  | Managed outside IAM. Users are uniquely identified in {{site.data.keyword.cloud_notm}} with the iam_id value, but can come from IBMid, {{site.data.keyword.appid_short}}, or SoftLayer | Managed in IAM. Identity federated to external identity management system.  | Managed in Active Directory | Managed outside IAM. Identity federated to external identity management system. |
| Service IDs | An ID for an app or service.  | Roles that are assigned to an app | User-assigned identity | Service accounts  |
| API key | A credential that is used for a user or service ID  | Access Key  | api-key | API key |
| Access groups  |  A way to organize users and service IDs where all members of the group are assigned the same access.  |Groups, roles | Active Directory groups | Google Groups |
| Trusted profiles  |  A way to assign access to federated users based on SAML attributes or for all applications running in a compute resource without the need of managing and rotating credentials.  |Roles | Managed identity | Workload identity |
| Policy  | Access assignment made up of a subject, target, and role. |  Policy  | Role assignment | Policy |
| Policy subject  | A user, service ID, or access group |  An IAM user, group, or a role | Security principal | A resource|
| Roles| A role is a collection of actions for a specific resource that are used as a building block to make an access policy.   | AWS-managed policy  | Role definition | Predefined roles |
| Custom roles | Customer-defined and named role, including only the actions chosen by the user.  |Customer-managed policies  | Custom roles | Custom roles  |
| Actions | What is allowed to be completed within the context of the platform or service | Actions | Permissions | Permissions  |
| Resources | Target of an access policy | Resources | Resources | Resources |
| Resource groups  | Logical organization container for IAM-enabled services | Tags  | Resource groups | Projects |
| Public access | Public access to specific resources is enabled through a default access group called Public Access. This feature can be disabled on each account. | Feature of Amazon S3 that can be enabled for specific resources, and can be disabled at the account or bucket level. | Public read access can be enabled for specific account types or resources. It can be disabled at the storage account or container level. | Google has an identifier for allAuthenticatedUsers that represents all service accounts and all users who are authenticated with a Google Account, which can also be granted access. |
| Auditing | Audit with Activity Tracker | Audit with AWS CloudTrail | Azure Logging and Auditing Activity logs | Audit with Audit logging |
| Enterprise-managed IAM | Centrally administer access and security settings from the root enterprise account. | AWS Control Tower |  |   |
{: row-headers}
{: caption="Table 1. {{site.data.keyword.cloud_notm}} IAM concept comparison" caption-side="top"}
{: summary="The first column is {{site.data.keyword.cloud_notm}} IAM concept. Then, each of the following columns has details as that concept relates the specific cloud provider that is listed in the column header."}

## Federating users to {{site.data.keyword.cloud_notm}}
{: #federation-iam}

{{site.data.keyword.cloud_notm}} offers two ways for you to federate your corporate identity provider (IdP), which simplifies login by giving your employees access to {{site.data.keyword.cloud_notm}} with their company username and password. The first option is to [federate with IBMid](https://ibm.box.com/v/IBMid-Federation-Guide){: external}, and the other option is to create an {{site.data.keyword.appid_full_notm}} service instance and use that as a way to federate users into an {{site.data.keyword.cloud_notm}} account. For more information, see [Enabling authentication from an external identity provider](/docs/account?topic=account-idp-integration).

In both types of federation, the user must be a member of the account, or have access to the account by a trusted profile to be able to complete operations. If trusted profiles are not configured, the account owner or administrator must invite individual IBMids into the {{site.data.keyword.cloud_notm}} account. Only if the invited IBMid accepts the invitation is the user added the account as an active user. In the case of {{site.data.keyword.appid_short}}, the user is automatically onboarded to {{site.data.keyword.cloud_notm}} without a need to invite each user to the account. In both types of federation, the users are active {{site.data.keyword.cloud_notm}} account users that can access the platform, including IAM-enabled resources, Cloud Foundry, and classic infrastructure all depending on their assigned access.

Trusted profiles deal with federated users differently. If the customer federates their corporate IdP, users from that IdP aren't added to an account as what we might consider a normal user. Instead, users' SAML-based IdP attributes are evaluated at login and if they meet all of the conditions for a trusted profile, they are prompted to apply one or more trusted profiles. Trusted profiles grant users the level of access they need to complete a specialized and specific set of tasks in a limited time-period, for example, 1-4 hours. These are usually critical tasks that you would want to avoid doing unintentionally in daily work. Users don't need to onboard to IBM Cloud, they're automatically added by way of the trust relationship. If a user leaves your company, you can simply delete the user's corporate identity in your directory, which then also revokes access to IBM Cloud. Time-based access allows frequent authentication checks for reduced security risks.
