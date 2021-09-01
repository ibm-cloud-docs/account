---

copyright:

  years: 2021

lastupdated: "2021-09-01"

keywords: trusted profile, identity and access management, federated users, compute resources, IAM trusted profile, trust relationship, establish trust, trust policy, trusted entity, assume access, apply access

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:important: .important}
{:note: .note}
{:pre: .pre}
{:ui: .ph data-hd-interface='ui'}
{:cli: .ph data-hd-interface='cli'}
{:api: .ph data-hd-interface='api'}
{:java: .ph data-hd-programlang='java'}
{:python: .ph data-hd-programlang='python'}
{:javascript: .ph data-hd-programlang='javascript'}
{:curl: .ph data-hd-programlang='curl'}
{:go: .ph data-hd-programlang='go'}


# Creating trusted profiles
{: #create-trusted-profile}

You can use a trusted profile to automatically grant federated users access to your account with conditions based on SAML attributes from your corporate directory. And, you can use trusted profile to set up fine-grained authorization for applications that are running in compute resources. As a result, you aren't required to create service IDs or API keys for the compute resources. 
{: shortdesc}

When you initially create a trusted profile, you can build trust only with either federated users or compute resources. After you created the trusted profile, you can add more conditions for federated users and compute resources in the same trusted profile.

You must be an administrator the IAM Identity Service in the account. For more information, see [IAM access](https://test.cloud.ibm.com/docs/account?topic=account-userroles). 
{: note}

## Establishing trust with federated users
{: #create-profile-federated-users}

Complete the following steps to define which federated users can access specific resources.

1. [Enable authentication from an external identity provider](/docs/account?topic=account-idp-integration). 
1. In the {{site.data.keyword.cloud_notm}} console, click **Manage** > **Access (IAM)**, and select **Trusted profiles**.
1. Click **Create profile**.
1. Describe your profile by providing a name and a description, then click **Continue**.

  In the description, provide a list of actions available for this trusted profile.
  {: tip}
  
1. (Optional) Establish trust.
  1. Select **Federated users** as a trusted entity type from the list.
  1. Select **Users federated by IBMid** or **Users federated by IBM Cloud AppID** as the authentication method and input the default identity prodiver (IdP) URL.
  1. Add conditions based on your IdP data to define how and when federated users can apply the profile.
    * By clicking **Add a condition**, you can define multiple conditions. Federated users must meet all the conditions to be included in the trusted profile.
    * Click **View identity provider (IdP) data** to search attribute names and values in your own personal data from your IdP. For more information, see [Using IdP data to build trusted profiles](/docs/account?topic=account-idp-integration#trusted-profiles-idp-data).
  1. Define the session duration for how long a user can apply the profile before they must reauthenticate, and click **Continue**.
1. (Optional) Create access policy. 
  1. Based on your level of access, you can assign IAM policies and classic infrastructure permissions. Select **IAM services** or **Account management** to continue.
  1. For **IAM services** and **Account management**, select the option for all resources or only specific resources based on attributes. Select any combination of roles and permissions to define the scope of access, and click **Add** > **Create**.
  
The Classic Infrastructure and Softlayer API is not currently enabled for users that log in to {{site.data.keyword.cloud_notm}} by applying a trusted profile. For more information, see [Troubleshooting account management](/docs/account?topic=account-troubleshoot-trusted-profile-classic). 
{: important}
    
## Establishing trust with compute resources
{: #create-profile-compute}

Complete the following steps to set up better control over granting access to compute resources.

{{site.data.keyword.containerlong_notm}} supports only trusted profiles for versions 1.21 and newer. Free {{site.data.keyword.containerlong_notm}} clusters create only earlier versions. You have the choice to create clusters with an earlier version with the standard plan, so be sure to select version 1.21 or newer.
{: important}

1. In the {{site.data.keyword.cloud_notm}} console, click **Manage** > **Access (IAM)**, and select **Trusted profiles**.
2. Click **Create profile**.
3. Describe your profile by providing a name and a description, and click **Continue**.
4. (Optional) Establish trust.
  1. Select **Compute resources** and select a compute service type from the list.
  2. If you select the option for **Any service resource**, you can define multiple conditions to filter resources for the selected compute service type by clicking **Add a condition**. These conditions are based on attributes, such as resource groups or location, and apply to all existing and future resources. Resources must meet all the conditions to be included in the trusted profile.

  The Kubernetes namespace and service account names that you enter do not have to exist already. Any future namespaces or service accounts with these names can establish trust. To list existing namespaces, log in to your cluster and run `kubectl get ns`. To list existing service accounts, log in to your cluster and run `kubectl get sa -n <namespace>`.
  {: note}

  3. If you select **Specific resources**, you can establish trust with one or more existing compute resource instances. For example, a Kubernetes cluster. 
5. (Optional) Create an access policy. 
  1. Based on your level of access, you can assign IAM policies and classic infrastructure permissions. Select **IAM services** or **Account management** to continue.
  2. For IAM services and account management services, select the option for all resources or only specific resources based on attributes. Select any combination of roles and permissions to define the scope of access, and click **Add** > **Create**.
