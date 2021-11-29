---

copyright:

  years: 2021

lastupdated: "2021-11-29"

keywords: trusted profile, generating IAM token, compute resource, kubernetes cluster, virtual server

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Generating an IAM token for a compute resource
{: #trusted-profile-iam-token}

You can request an Identity and Access Management token for Virtual server for VPC that represents the trusted profile for your compute resources. The IAM access token is suitable for use as a bearer token in calls that require user or service credentials.
{: shortdesc}

For Kubernetes, you don't need to take steps to exchange a compute resource (CR) token for an IAM token; this is done automatically by the service for new clusters that run Kubernetes version 1.21 or later. Trusted profiles are not supported for earlier versions of Kubernetes. See [Authorizing pods in your cluster to IBM Cloud services with IAM trusted profiles](/docs/containers?topic=containers-pod-iam-identity) for more information.

To generate IAM tokens for your compute resources, you must be at least an administrator on all Identity and Access enabled services within the account.
{: note}

## Exchanging your tokens
{: #token-exchange}

1. Set up a trusted profile where you establish trust with compute resources. Select **Virtual server for VPC** as a compute service type. To complete this step, follow the instructions of [Setting up trusted profiles](/docs/account?topic=account-create-trusted-profile#create-profile-compute).
1. Retrieve a compute resource token (CR-token), which is specific to the resource. For example, a virtual server instance. 

   For Virtual server for VPC, see [Acquire a JSON web token](/docs/vpc?topic=vpc-imd-configure-service#imd-json-token).

1. To retrieve an IAM access token that represents the trusted profile, provide the CR-token for IAM. One CR-token might resolve to multiple trusted profiles, therefore you must pass either `profile_id` or `profile_name` as a parameter. If both parameters are specified, they must resolve to the same compute resource, otherwise the API call fails.

   ```curl
    $ curl -X POST \
        -H "Content-Type: application/x-www-form-urlencoded"   
        -H "Accept: application/json"                          
        -d grant_type=urn:ibm:params:oauth:grant-type:cr-token 
        -d cr_token=$(CRTOKEN)                                 
        -d profile_name=TestProfile                            
        https://iam.test.cloud.ibm.com/identity/token
   ```
   {: codeblock}

   The compute resource and the trusted profile must be in the same account. Trusted profiles from another account that would have matching rules are not considered.
   {: note}
