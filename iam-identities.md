---

copyright:

  years: 2022

lastupdated: "2022-01-31"

keywords: identities, IAM, how IAM works

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}


# Identities in IBM Cloud
{: #identity-overview}

The two major concepts of {{site.data.keyword.cloud_notm}} IAM are identity and access management. For more information, review the following sections and [Access management concepts](/docs/account?topic=account-access-management-overview&interface=ui).

The identity concept consists of user identities, service and app identities, API keys, resources, and trusted profiles. Users are identified by their IBMid, SoftLayer, {{site.data.keyword.appid_short}} user ID, or federated user attributes. Service IDs are a second type of identity that is used in an account. Service IDs are used to provide a separate identity for services and applications. You can create a service ID to be used by an application that needs access to your {{site.data.keyword.cloud_notm}} services so that individual user credentials don't need to be used. As an alternative to creating service IDs and managing the API key lifecycle for applications, you can create [trusted profiles for compute resources](https://cloud.ibm.com/docs/account?topic=account-iamoverview#trusted-profiles-feature-resources) to define fine-grained authorization for all applications that are running in a compute resource.

Similar to other identities within IAM, trusted profiles are treated as a subject in IAM policies. Usually, for a user to take an action on a resource within an account, that identity must explicitly be added to the account. With trusted profiles, it is possible for a user to complete such actions without being invited to an account. Instead, they are automatically granted access to resources when they apply the trusted profile identity during login. Only users federated by an external IdP can be mapped to trusted profiles during login by evaluating SAML-based attributes to determine which profiles their identity can apply. 

Likewise, instead of having to create a service ID, generate an API key, and get the application to store and validate that key, you can assign an IAM trusted profile identity directly to a compute resource instance and acquire identity tokens. Trust with compute resources is established by way of conditions based on resource attributes, or creating a direct link to a specific resource.

{{site.data.keyword.cloud_notm}} API keys are used to authenticate with an API or CLI as a user or service ID. These API keys are provided through {{site.data.keyword.cloud_notm}} IAM and can't be used generally to authenticate with IBMid outside of {{site.data.keyword.cloud_notm}}. You can also use a single classic infrastructure API key to access classic infrastructure APIs; however, this is not required as you can use {{site.data.keyword.cloud_notm}} API keys to access the same APIs.

The final piece of the identity concept in IAM is {{site.data.keyword.cloud_notm}} resources, which are identified by their cloud resource names (CRN). CRNs are used for service-to-service authorizations. For more information, see [Cloud Resource Names](/docs/account?topic=account-crn).