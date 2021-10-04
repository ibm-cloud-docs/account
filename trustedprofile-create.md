---

copyright:

  years: 2021

lastupdated: "2021-10-04"

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

You must be an administrator the IAM Identity Service in the account. For more information, see [IAM access](/docs/account?topic=account-userroles). 
{: note}

## Establishing trust with federated users
{: #create-profile-federated-ui}
{: ui}

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
   1. You can assign **Classic infrastructure** access by selecting a user, device, or service, then any combination of granular permissions.

You can assign only classic infrastructure access if your account is linked to a Softlayer account.
{: note}
    
## Establishing trust with compute resources
{: #create-profile-compute-ui}
{: ui}

Complete the following steps to set up better control over granting access to compute resources.

{{site.data.keyword.containerlong_notm}} supports only trusted profiles for versions 1.21 and newer. Free {{site.data.keyword.containerlong_notm}} clusters create only earlier versions. You have the choice to create clusters with an earlier version with the standard plan, so be sure to select version 1.21 or newer.
{: important}

1. In the {{site.data.keyword.cloud_notm}} console, click **Manage** > **Access (IAM)**, and select **Trusted profiles**.
2. Click **Create profile**.
3. Describe your profile by providing a name and a description, and click **Continue**.
4. (Optional) Establish trust.
   1. Select **Compute resources** and select a compute service type from the list.
   2. If you select the option for **All service resources**, you can define multiple conditions to filter resources for the selected compute service type by clicking **Add a condition**. These conditions are based on attributes, such as resource groups or location, and apply to all existing and future resources. Resources must meet all the conditions to be included in the trusted profile.
   
   The Kubernetes namespace and service account names that you enter do not have to exist already. Any future namespaces or service accounts with these names can establish trust. To list existing namespaces, log in to your cluster and run `kubectl get ns`. To list existing service accounts, log in to your cluster and run `kubectl get sa -n <namespace>`.
   {: note}

   3. If you select **Specific resources**, you can establish trust with one or more existing compute resource instances. For example, a Kubernetes cluster. 
   
5. (Optional) Create an access policy. 
   1. Based on your level of access, you can assign IAM policies and classic infrastructure permissions. Select **IAM services** or **Account management** to continue.
   2. For IAM services and account management services, select the option for all resources or only specific resources based on attributes. Select any combination of roles and permissions to define the scope of access, and click **Add** > **Create**.
   3. You can assign **Classic infrastructure** access by selecting a user, device, or service, then any combination of granular permissions.

You can assign only classic infrastructure access if your account is linked to a Softlayer account.
{: note}

## Establishing trust with federated users by using the API
{: #create-profile-federated-api}
{: api}

Complete the following steps to define which federated users can access specific resources:

1. [Enable authentication from an external identity provider](/docs/account?topic=account-idp-integration). 
2. Create a trusted profile by specifying your account ID.

   ```bash
   curl -X POST 'https://iam.cloud.ibm.com/v1/profiles' -H 'Authorization: Bearer TOKEN' -H 'Content-Type: application/json' -H 'Accept: application/json' -d '{
   "name": "My Nice Profile",
   "description": "My Nice Profile - desc",
   "account_id": "ACCOUNT_ID"
   }'
   ```
   {: codeblock}

   In the description, provide a list of actions available for this trusted profile.
   {: tip}

3. Create conditions for your trusted profile. For federated users, set the `type` attribute to `Profile-SAML`. The `realm-name` is the IdP URL. For more information, see the [IAM Identity Services API](apidocs/iam-identity-token-api#create-claim-rule-request). 

   ```bash
   curl -X POST 'https://iam.cloud.ibm.com/v1/profiles/PROFILE_ID/rules' -H 'Authorization: Bearer TOKEN' -H 'Content-Type: application/json' -H 'Accept: application/json' -d '{
   "type": "Profile-SAML",
   "realm_name": "https://www.example.org/my-nice-idp",
   "expiration": 43200,
   "conditions": [
   {
   "claim": "groups",
   "operator": "EQUALS",
   "value": "\"cloud-docs-dev\""
      }
      ] 
   }'
   ```
   {: codeblock}

   There is a limit of 20 claim rules per trusted profile.
   {: note}

4. Create an access policy. For more information, see [IAM Policy Management API?](/apidocs/iam-policy-management) 

   ```bash
   curl -X POST 'https://iam.cloud.ibm.com/v1/policies' -H 'Authorization: Bearer $TOKEN' -H 'Content-Type: application/json' -d '{
   "type": "access",
   "description": "Editor role for SERVICE_NAME's RESOURCE_NAME",
   "subjects": [
      {
         "attributes": [
         {
            "name": "iam_id",
            "value": "IBMid-123453user"
         }
         ]
      }'
   ],
   "roles":[
      {
         "role_id": "crn:v1:bluemix:public:iam::::role:Editor"
      }
   ],
   "resources":[
      {
         "attributes": [
         {
            "name": "accountId",
            "value": "$ACCOUNT_ID"
         },
         {
            "name": "serviceName",
            "value": "$SERVICE_NAME"
         },
         {
            "name": "resource",
            "value": "$RESOURCE_NAME",
            "operator": "stringEquals"
         }
         ]
      }
   ]
   }'
   ```
   {: codeblock}

## Establishing trust with compute resources
{: #create-profile-compute-api}
{: api}

Complete the following steps to set up better control over granting access to compute resources.

{{site.data.keyword.containerlong_notm}} supports only trusted profiles for versions 1.21 and newer. Free {{site.data.keyword.containerlong_notm}} clusters create only earlier versions. You have the choice to create clusters with an earlier version with the standard plan, so be sure to select version 1.21 or newer.
{: important}

1. Create a trusted profile by specifying your account ID.

   ```bash
   curl -X POST 'https://iam.cloud.ibm.com/v1/profiles' -H 'Authorization: Bearer TOKEN' -H 'Content-Type: application/json' -H 'Accept: application/json' -d '{
   "name": "My Nice Profile",
   "description": "My Nice Profile - desc",
   "account_id": "ACCOUNT_ID"
   }'
   ```
   {: codeblock}

   In the description, provide a list of actions available for this trusted profile.
   {: tip}

2. Create a claim rule for your trusted profile that follows the principle of least privilege by specifying conditions that target only the resources that need access. Conditions apply to all existing future resources. You can also create a direct link with specific, existing resources. 

   **Create conditions**
   For compute resources, set the `type` attribute to `Profile-CR`. For more information, see the [IAM Identity Services API](/apidocs/iam-identity-token-api#create-claim-rule-request). 

      ```bash
      curl -X POST 'https://iam.cloud.ibm.com/v1/profiles/PROFILE_ID/rules' -H 'Authorization: Bearer TOKEN' -H 'Content-Type: application/json' -H 'Accept: application/json' -d '{
      "type": "Profile-CR",
      "conditions": [
      {
      "claim": "namespace",
      "operator": "EQUALS",
      "value": "\"default123\""
         }
         ] 
      }'
      ```
      {: codeblock}

      There is a limit of 20 claim rules per trusted profile.
      {: note}

   **Create a direct link**
   ```bash
   curl -X POST 'https://iam.cloud.ibm.com/v1/profiles/PROFILE_ID/links' -H 'Authorization: Bearer TOKEN' -H 'Content-Type: application/json' -H 'Accept: application/json' -d '{
      "name": "my link",
      "cr_type": "VSI",
      "link": {
   "crn": "crn:v1:staging:public:iam-identity::a/18e3020749ce4744b0b472466d61fdb4::computeresource:Fake-Compute-Resource",
   "namespace": "default",
   "name": "my compute resource name"
      }
   }'
   ```
   {: codeblock}

3. Create an access policy. For more information, see [IAM Policy Management API?](/apidocs/iam-policy-management)

   ```bash
   curl -X POST 'https://iam.cloud.ibm.com/v1/policies' -H 'Authorization: Bearer $TOKEN' -H 'Content-Type: application/json' -d '{
   "type": "access",
   "description": "Editor role for SERVICE_NAME's RESOURCE_NAME",
   "subjects": [
      {
         "attributes": [
         {
            "name": "iam_id",
            "value": "IBMid-123453user"
         }
         ]
      }'
   ],
   "roles":[
      {
         "role_id": "crn:v1:bluemix:public:iam::::role:Editor"
      }
   ],
   "resources":[
      {
         "attributes": [
         {
            "name": "accountId",
            "value": "$ACCOUNT_ID"
         },
         {
            "name": "serviceName",
            "value": "$SERVICE_NAME"
         },
         {
            "name": "resource",
            "value": "$RESOURCE_NAME",
            "operator": "stringEquals"
         }
         ]
      }
   ]
   }'
   ```
   {: codeblock}
   