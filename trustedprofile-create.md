---

copyright:

  years: 2021, 2022


lastupdated: "2022-06-22"

keywords: trusted profile, identity and access management, federated users, compute resources, IAM trusted profile, trust relationship, establish trust, trust policy, trusted entity, assume access, apply access, access group

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}


# Creating trusted profiles
{: #create-trusted-profile}

You can use trusted profiles to automatically grant federated users access to your account with conditions based on SAML attributes from your corporate directory. Trusted profiles can also be used to set up fine-grained authorization for applications that are running in compute resources. This way, you aren't required to create service IDs or API keys for the compute resources. 
{: shortdesc}

When you initially create a trusted profile, you can build trust with either federated users or compute resources. After the trusted profile is created, you can add more conditions for federated users and compute resources in the same trusted profile.

You can use {{site.data.keyword.cloudaccesstrailshort}} to monitor which federated users and compute resources apply a trusted profile. For more information, see [Monitoring login sessions for trusted profiles](/docs/account?topic=account-trusted-profile-monitor).
{: tip}

## Before you begin
{: #tp-roles-reqs}

If you have the following access, you can create trusted profiles:

- Account owner
- Administrator role on all account management services
- Administrator role on the IAM Identity Service. For more information, see [IAM Identity service](/docs/account?topic=account-account-services#identity-service-account-management). 

## Establishing trust with federated users
{: #create-profile-federated-ui}
{: ui}

Complete the following steps to define which federated users can access specific resources:

1. [Enable authentication from an external identity provider](/docs/account?topic=account-idp-integration). 
1. In the {{site.data.keyword.cloud_notm}} console, click **Manage** > **Access (IAM)**, and select **Trusted profiles**.
1. Click **Create profile**.
1. Describe your profile by providing a name and a description, then click **Continue**.

      In the description, provide a list of actions available for this trusted profile.
      {: tip}

1. (Optional) Establish trust.
   1. Select **Federated users** as a trusted entity type from the list.
   1. Select **Users federated by IBMid** or **Users federated by IBM Cloud AppID** as the authentication method and input the default identity prodiver (IdP) you enabled in step 1.

   If the users that you are creating a trusted profile for use {{site.data.keyword.appid_full_notm}}, create the trusted profile as an App ID user, and likewise for IBMid. This way, your own SAML attributes can give you an idea of how to structure the trusted profile conditions. Other users with the same IdP can have different SAML attributes. Use your own attributes only as a hint. To use attributes in a claim that are different than your own, input them manually. 
   {: tip}

   1. Add conditions based on your IdP data to define how and when federated users can apply the profile.
      * By clicking **Add a condition**, you can define multiple conditions. Federated users must meet all the conditions to be included in the trusted profile. For more information about the fields that are used to create conditions, see [IAM condition properties](/docs/account?topic=account-iam-condition-properties).
      * Click **View identity provider (IdP) data** to search attribute names and values in your own personal data from your IdP. For more information, see [Using IdP data to build trusted profiles](/docs/account?topic=account-idp-integration#trusted-profiles-idp-data).

1. Define the session duration for how long a user can apply the profile before they must reauthenticate.
1. Click **Continue**.
1. (Optional) Assign access. 
   * Assign access to the trusted profile by adding it to one or more access groups. This way, you can use the policies that exist in the access groups you've created. 
      1. Select **Access groups** and select all the groups that you want to add the trusted profile to. You can assign users to only the access groups that you have access to manage.  
      1. Click **Add**. 
   * Assign access to the trusted profile with an access policy.  
      1. Select **Access policy**. Based on your level of access, you can assign IAM policies and classic infrastructure permissions.
      1. Select a single service or a group of services, such as **All Identity and Access enabled services**, **All Account Management services**, or **All IAM Account Management services**. Then, click **Next**. 
      1. Scope the access to **All resources** or **Specific resources** based on selected attributes. Then, click **Next**. 
      1. Select any combination of roles and permissions to define the scope of access, and click **Review**. 
      1. Click **Add** to add your policy configuration to your summary.
      1. You can assign **Classic infrastructure** access by selecting a user, device, or service, then any combination of granular permissions.
1. Click **Create**. 
   
For more information about the fields that are used to create conditions for trusted profiles, see [IAM policy properties](/docs/account?topic=account-iam-condition-properties).

You can assign only classic infrastructure access if your account is linked to a Softlayer account.
{: note}

## Establishing trust with compute resources in the console
{: #create-profile-compute}
{: ui}

Complete the following steps to set up better control over granting access to compute resources.

{{site.data.keyword.containerlong_notm}} supports only trusted profiles for versions 1.21 and newer. Free {{site.data.keyword.containerlong_notm}} clusters create only earlier versions. You have the choice to create clusters with an earlier version with the standard plan, so be sure to select version 1.21 or newer.
{: important}

1. In the {{site.data.keyword.cloud_notm}} console, click **Manage** > **Access (IAM)**, and select **Trusted profiles**.
1. Click **Create profile**.
1. Describe your profile by providing a name and a description, and click **Continue**.
1. (Optional) Establish trust.
   1. Select **Compute resources** and select a compute service type from the list.
   1. If you select the option for **All service resources**, you can define multiple conditions to filter resources for the selected compute service type by clicking **Add a condition**. These conditions are based on attributes, such as resource groups or location, and apply to all existing and future resources. Resources must meet all the conditions to be included in the trusted profile.

   The Kubernetes namespace and service account names that you enter do not have to exist already. Any future namespaces or service accounts with these names can establish trust. To list existing namespaces, log in to your cluster and run `kubectl get ns`. To list existing service accounts, log in to your cluster and run `kubectl get sa -n <namespace>`. You can also enter `default` for both. For more information, see [Using Trusted Profiles in your Kubernetes and OpenShift Clusters](https://www.ibm.com/cloud/blog/using-trusted-profiles-in-your-kubernetes-and-openshift-clusters).
   {: tip}

   1. If you select **Specific resources**, you can establish trust with one or more existing compute resource instances. For example, a Kubernetes cluster. 

1. (Optional) Assign access. 
   * Assign access to the trusted profile by adding it to one or more access groups. This way, you can use the policies that exist in the access groups you've created. 
      1. Select **Access groups** and select all the groups that you want to add the trusted profile to. You can assign users to only the access groups that you have access to manage.  
      1. Click **Add**. 
   * Assign access to the trusted profile with an access policy.  
      1. Select **Access policy**. Based on your level of access, you can assign IAM policies and classic infrastructure permissions.
      1. Select a single service or a group of services, like **All Identity and Access enabled services**, **All Account Management services**, or **All IAM Account Management services**. Then, click **Next**. 
      1. Scope the access to **All resources** or **Specific resources** based on selected attributes. Then, click **Next**. 
      1. Select any combination of roles and permissions to define the scope of access, and click **Review**. 
      1. Click **Add** to add your policy configuration to your summary.
      1. You can assign **Classic infrastructure** access by selecting a user, device, or service, then any combination of granular permissions.
1. Click **Create**. 

You can assign only classic infrastructure access if your account is linked to a Softlayer account.
{: note}


## Establishing trust with federated users by using the CLI
{: #create-profile-federated-cli}
{: cli}

Complete the following steps to define which federated users can access specific resources:

1. [Enable authentication from an external identity provider](/docs/account?topic=account-idp-integration). 
1. Create a trusted profile by running the following command:

   ```bash
   ibmcloud iam trusted-profile-create my-profile -d "sample trusted profile" 
   ```
   {: codeblock}
   
   For more information, see the [CLI reference](/docs/account?topic=cli-ibmcloud_commands_iam#ibmcloud_iam_trusted_profile_create). 

1. To create conditions for your trusted profile, run the `ibmcloud iam trusted-profile-rule-create` command:

   ```bash
   ibmcloud iam trusted-profile-rule-create my-profile --name my-rule --type Profile-SAML --conditions claim:cn,operator:EQUALS,value:my_user --realm-name https://w3id.sso.ibm.com/auth/sps/samlidp2/saml20 --expiration 1200
   ```
   {: codeblock}

   For more information, see the [CLI reference](/docs/account?topic=cli-ibmcloud_commands_iam#ibmcloud_iam_trusted_profile_rule_create). 
   
1. Create an access policy with the `Viewer` role for all resources in the account by running the following command:

   ```bash
   ibmcloud iam trusted-profile-policy-create --roles Viewer
   ```
   {: codeblock}
   
   For more information, see the [CLI reference](/docs/account?topic=cli-ibmcloud_commands_iam#ibmcloud_iam_trusted_profile_policy_create). 


## Establishing trust with compute resources by using the CLI
{: #create-profile-compute-cli}
{: cli}

Complete the following steps to set up better control over granting access to compute resources.
 
{{site.data.keyword.containerlong_notm}} supports only trusted profiles for versions 1.21 and newer. Free {{site.data.keyword.containerlong_notm}} clusters create only earlier versions. You have the choice to create clusters with an earlier version with the standard plan, so be sure to select version 1.21 or newer.
{: important}
  
1. Create a trusted profile by running the following command:

   ```bash
   ibmcloud iam trusted-profile-create sample-compute-profile -d "sample trusted profile for compute resources" 
   ```
   {: codeblock}

   For more information, see the [CLI reference](/docs/account?topic=cli-ibmcloud_commands_iam#ibmcloud_iam_trusted_profile_create). 
   
1. Create conditions for your trusted profile by using the `ibmcloud iam trusted-profile-rule-create` command:

   ```bash
   ibmcloud iam trusted-profile-rule-create sample-compute-profile --name cr-rule --type Profile-CR --conditions claim:namespace,operator:EQUALS,value:default --conditions claim:crn,operator:EQUALS,value:crn:test:bluemix:public:containers-kubernetes:us-south:a/test:: --cr-type IKS_SA
   ```
   {: codeblock}

   For more information, see the [CLI reference](/docs/account?topic=cli-ibmcloud_commands_iam#ibmcloud_iam_trusted_profile_rule_create). 
   
   You can also create a direct link:
   
   ```bash
   ibmcloud iam trusted-profile-link-create sample-compute-profile --name my_link --cr-type IKS_SA --link-name default  --link-namespace default --link-crn my_compute_resource_crn
   ```
   {: codeblock}

   For more information, see the [CLI reference](/docs/account?topic=cli-ibmcloud_commands_iam#ibmcloud_iam_trusted_profile_link_create). 
   
1. Create an access policy by running the following command:

   ```bash
   ibmcloud iam trusted-profile-policy-create --roles Viewer
   ```
   {: codeblock}   

   For more information, see the [CLI reference](/docs/account?topic=cli-ibmcloud_commands_iam#ibmcloud_iam_trusted_profile_policy_create). 

## Establishing trust with federated users by using the API
{: #create-profile-federated-api}
{: api}

Complete the following steps to define which federated users can access specific resources:

1. [Enable authentication from an external identity provider](/docs/account?topic=account-idp-integration). 
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

1. Create conditions for your trusted profile. For federated users, set the `type` attribute to `Profile-SAML`. The `realm-name` is the IdP URL. For more information, see the [IAM Identity Services API](/apidocs/iam-identity-token-api). 

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

1. Create an access policy. For more information, see [IAM Policy Management API?](/apidocs/iam-policy-management).

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

## Establishing trust with compute resources by using the API
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

1. Create a claim rule for your trusted profile that follows the principle of least privilege by specifying conditions that target only the resources that need access. Conditions apply to all existing future resources. You can also create a direct link with specific, existing resources. 

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
      "crn": "crn:v1:bluemix:public:iam-identity::a/18e3020749ce4744b0b472466d61fdb4::computeresource:Fake-Compute-Resource",
      "namespace": "default",
      "name": "my compute resource name"
         }
      }'
      ```
      {: codeblock}

1. Create an access policy. For more information, see [IAM Policy Management API?](/apidocs/iam-policy-management).

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
   
