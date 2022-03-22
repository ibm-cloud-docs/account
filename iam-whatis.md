---

copyright:

  years: 2017, 2022

lastupdated: "2022-03-22"


keywords: what is IAM, IAM features, IAM API, how IAM works

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}


# How {{site.data.keyword.cloud_notm}} IAM works
{: #iamoverview}

Learn about what {{site.data.keyword.cloud_notm}} Identity and Access Management (IAM) is, how IAM works, what features are available, and how to access the console, CLI, and APIs to work with IAM in your account.
{: shortdesc}

IAM enables you to securely authenticate users for platform services and control access to resources consistently across {{site.data.keyword.cloud_notm}}. A set of {{site.data.keyword.cloud_notm}} services is enabled to use {{site.data.keyword.cloud_notm}} IAM for access control, and are organized into [resource groups](/docs/account?topic=account-rgs) within your account so you can give users access quickly to more than one resource at a time. Each of these services is labeled as "IAM-enabled" in the catalog. You can use IAM access policies to assign users and service IDs access to resources within your account. And, you can group users and service IDs into an [access group](/docs/account?topic=account-groups) to easily give all members of the group the same level of access.

![IAM access control in an account by using access groups](images/IAM-access-groups-diagram.svg "How IAM access works in an account by using access groups"){: caption="Figure 1. How IAM access works in an account by using access groups" caption-side="bottom"}

You can also use [trusted profiles](/docs/account?topic=account-create-trusted-profile) to group and grant access to users, service, and app identities. By specifying conditions based on SAML attributes for users whose identity is federated from your external identity provider (IdP), users can be granted access to resources without having to be invited to the account if they meet those conditions. For service and app identities, you can define fine-grained authorization for all applications that are running in a compute resource without creating service IDs or manage the API key lifecycle for applications.

![IAM access control in an account by using trusted profiles](images/IAM-trusted-profiles-diagram-2.svg "How IAM access works in an account by using trusted profiles"){: caption="Figure 2. How IAM access works in an account by using trusted profiles" caption-side="bottom"}

For services that don't support the use of {{site.data.keyword.cloud_notm}} IAM policies for managing access, you can use [Cloud Foundry access](/docs/account?topic=account-mngcf) or [classic infrastructure permissions](/docs/account?topic=account-mngclassicinfra).
{: note}

## What features are provided?
{: #features}

{{site.data.keyword.cloud_notm}} IAM provides a wide range of features for your identity and access management needs. 

### User management
{: #usermgmt-feature}

With unified user management, you can add and delete users in an account for both platform and classic infrastructure services. You can organize a group of users in an access group to make assigning access for more than one user or service ID at a time a quick and easy task.

### Fine-grained access control
{: #fgaccess-feature}

Access for users, service IDs, access groups, and trusted profiles are defined by a policy. Within the policy, the scope of access can be assigned to a set of resources in a resource group, a single resource, or account management services. After the target is set, you can define what actions are allowed by the subject of the policy by selecting access roles. Roles provide a way to tailor the level of access that is granted for the subject of the policy to perform actions on the target of policy, whether it is platform management tasks within the account or accessing a service's UI or completing API calls.

### Access groups for streamlined access management
{: #access-groups-quick-access}

Quickly and easily assign access for a group or users or service IDs organized in an access group by assigning access to the group, and then add or remove users or service IDs as needed to grant or deny access to account resources. Access groups enable you to manage a minimal number of policies in the account. For more information, see [Setting up access groups](/docs/account?topic=account-groups).

### Trusted profiles for eliminating the need to manage credentials
{: #trusted-profiles-feature}
{: support}
{: help}

Quickly and easily assign access for a group of federated users or compute resources that are organized in a trusted profile. You assign access to the profile, and then add or remove conditions as needed to grant or deny access to account resources. By using trusted profiles, you can centrally manage the access lifecycle to multiple {{site.data.keyword.cloud_notm}} assets. For more information, see [Setting up trusted profiles](/docs/account?topic=account-create-trusted-profile).

#### Federated users
{: #trusted-profiles-feature-fedusers}

Your users might already have identities outside of {{site.data.keyword.cloud_notm}}, in your corporate directory. If your users need to work with {{site.data.keyword.cloud_notm}} resources or work with applications that access those resources, then those users also need {{site.data.keyword.cloud_notm}} credentials. You can use a trusted profile to specify permissions for users whose identity is federated from your organization or an external IdP. By using your IdP, you can provide a way for users in your company to use single sign-on (SSO). To connect your federated users with {{site.data.keyword.cloud_notm}} resources, see [Federating users to {{site.data.keyword.cloud_notm}}](#federation-iam).

#### Compute resources
{: #trusted-profiles-feature-resources}

By using trusted profiles, you can define fine-grained authorization for all applications that are running in a compute resource without creating service IDs or managing the API key lifecycle for applications. The trusted profiles provide better control for granting access to compute resources.

*  Application developers can programmatically retrieve a token that is associated with the compute resource identity that they are running on. That token is used to get the trusted profile identity token, which is used to access services and resources on {{site.data.keyword.cloud_notm}}.
*  Applications running on a compute resource can have a flexible, but secure way to access other {{site.data.keyword.cloud_notm}} services from within compute resources. For example, it's more secure not having to store API keys.
*  All compute resource instances that share certain conditions such as name, namespace, tags, or location, their identities are mapped to a common profile and can share access to {{site.data.keyword.cloud_notm}} resources. This common identity makes it possible to give the applications within various compute resources access to an external resource one time rather than cluster-by-cluster.

You can monitor which federated users and compute resources apply a trusted profile by looking at {{site.data.keyword.at_short}}. The fields `Initiator.authnId` and `Initiator.authnName` hold the details for the authenticated user that applies a profile, while `Initiator.id` and `Initiatior.name` hold the details of the profile that is applied. For compute resources the `authn` fields hold the CRN that uniquely identifies the resource that applies a profile. For more information, see [Required AT field events](https://cloud.ibm.com/docs/observability?topic=observability-at_req_fields#initiator.authnId).
{: note}

### API keys for user authentication
{: #apikey-feature}

You can create multiple API keys for a user to support key rotation scenarios, and the same key can be used for accessing multiple services. {{site.data.keyword.cloud_notm}} API keys enable users who use two-factor authentication or a federated ID to automate authentication to the console from the command line. A user can also have a single classic infrastructure API key that can be used to access classic infrastructure APIs; however, this is not required as you can use {{site.data.keyword.cloud_notm}} API keys to access the same APIs. For more information, see [Understanding API keys](/docs/account?topic=account-manapikey).

### Service IDs
{: #svcid-feature}

A service ID identifies a service or application similar to how a user ID identifies a user. These are IDs that can be used by applications to authenticate with an {{site.data.keyword.cloud_notm}} service. Policies can be assigned to each service ID to control the level of access that is allowed by an application that uses the service ID, and an API key can be created to enable the authentication. For more information, see [Creating and working with service IDs](/docs/account?topic=account-serviceids).

Infrastructure-as-a-Service (IaaS) doesn't support operations that are made by service IDs. If an account includes IaaS and PaaS, administrative functions that are made by a service ID might not work as intended if the operation depends on API calls to IaaS. In an account that includes IaaS, be sure that account administrators complete the administrative functions. For example, functional IDs can be used for administrative functions. In some cases, IBM support might be able to assist with some administrative functions that span both IaaS and PaaS.
{: note}

### Multifactor authentication
{: #mfa-feature}

You can require multifactor authentication (MFA) for every user in the account or just users with non-federated IDs who do not use SSO. All users with an IBMid use a time-based one-time passcode (TOTP) MFA factor, and any users with a different type of ID must be enabled to use the TOTP, security questions, or external authentication factor separately. For more information, see [Types of multifactor authentication](/docs/account?topic=account-types).

### Service to service authorizations
{: #service-authorizations-feature}

In a scenario that you need to provide one service access to another, you can create a policy by using a service to service authorization. For more information, see [Using authorizations to grant access between services](/docs/account?topic=account-serviceauth).

## How do I use {{site.data.keyword.cloud_notm}} IAM?
{: #howto}

You can access and use {{site.data.keyword.cloud_notm}} IAM through the Access (IAM) UI, CLI, or API.

* To access {{site.data.keyword.cloud_notm}} IAM by using the console, go to **Manage** > **Access (IAM)**.
* Go to [Managing IAM access, API keys, service IDs, and access groups](/docs/cli?topic=cli-ibmcloud_commands_iam) to review the available CLI commands.
* Go to the following API docs to review the available APIs:
    * [IAM Identity Services API](/apidocs/iam-identity-token-api){: external} 
    * [IAM Access Groups API](/apidocs/iam-access-groups){: external} 
    * [IAM Policy Management API](/apidocs/iam-policy-management){: external} 
