---

copyright:
  years: 2019, 2025
lastupdated: "2025-01-22"

keywords: IBM Cloud account, account differences, account overview, account components, resource, API key, users

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}


# What's in an account?
{: #overview}

Your {{site.data.keyword.Bluemix}} account includes many interacting components and systems for resource, user, and access management. Concepts like how certain components are connected or how access works help you in understanding how to set up your account.
{: shortdesc}

The following diagram contains two main concepts for the components in the account hierarchy that are important to understand. The use of the solid lines and the dotted lines help illustrate that some components are contained within others, for example, users are added to access groups. However, some components interact with others for providing access instead of membership. For example, users are given access to resource groups but are not members of a resource group the same way they are for access groups.



Users
:   Users are invited to the account and given access to the resources in the account.

Service IDs
:   A service ID identifies a service or application similar to how a user ID identifies a user. You can use a service ID that you create to enable an application outside of {{site.data.keyword.Bluemix_notm}} access to your services. You can assign specific access policies to the service ID that restrict permissions for using specific services, or even combine permissions for accessing different services. Since service IDs are not tied to a specific user, if a user happens to leave an organization and is deleted from the account, the service ID remains, ensuring that your application or service stays up and running. For more information, see [Creating and working with service IDs](/docs/account?topic=account-serviceids).

Trusted profiles
:   A trusted profile is a grouping of federated users, compute resources, {{site.data.keyword.Bluemix_notm}} services, service IDs, or a combination of entities, to which the same {{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM) access can be granted. When applying a trusted profile, temporary security credentials are provided for the duration of a session. All identities that are allowed to apply a single profile inherit the same access. For more information, see [Creating trusted profiles](/docs/account?topic=account-create-trusted-profile).

Service instances or resources
:   Services in {{site.data.keyword.Bluemix_notm}} are resource group-based. Service instances that can be added to a resource group and managed by using IAM are called resources. For more information, see [Creating resources](/docs/account?topic=account-manage_resource).

API keys
:   An API key is a unique code that is passed in to an API to identify the calling application or user. You can use platform API keys, which are associated with user identities, and you can create other API keys for service IDs. For more information, see [Understanding API keys](/docs/account?topic=account-manapikey).

Access groups
:   You can create an access group to organize a set of users, service IDs, and trusted profiles into a single entity and easily assign permissions. You can assign a single policy to the group instead of assigning the same access multiple times per individual user or service ID. For more information, see [Setting up access groups](/docs/account?topic=account-groups).

Resource groups
:   You can use a resource group to organize your account resources in customizable groupings so that you can quickly assign users access to more than one resource at a time. Any account resource that is managed by using IAM access control belongs to a resource group within your account. Users are not added to resource groups, but users are provided access to the resources within or can manage the resource group. Users given access to manage the resource group can create new instances within the group, manage other user's access to work with the group, or edit the group name based on the assigned IAM role. You can have a maximum of 1000 resource groups per account. For more information, see [Best practices for organizing resources and assigning access](/docs/account?topic=account-account_setup).


Another important aspect of the previous diagram is the depiction of the two types of access management systems that you can use to provide account users access to resources within the account.

   * You can use IAM [access roles](/docs/account?topic=account-userroles) to provide users access to all resources that belong to a resource group. You can also give users access to manage resource groups and create new service instances that are assigned to a resource group.
   * You can use [classic infrastructure permissions](/docs/account?topic=account-mngclassicinfra) to grant users more granular permissions for classic infrastructure resources. You assign device access and VPN subnet access separately.
