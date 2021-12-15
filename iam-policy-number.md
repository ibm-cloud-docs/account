---

copyright:
  years: 2020, 2021
lastupdated: "2021-12-15"

keywords: maximum limits, limits, maximum policies, check for limits, check policy number, increase policy limit, total number of account policies, increase account limit

subcollection: account

---


{{site.data.keyword.attribute-definition-list}}

# Increasing account limits
{: #account-limits}

Default maximum limits are set on entities in your account such as access policies, service IDs, trusted profiles, identity providers (IdPs), and API keys. However, specific use cases can require an extended limit and you must request an increase for your chosen entity. You must be the account owner or administrator for all account management services to check how many policies exist in the account.
{: shortdesc}

To review the default limits for your account, see [Known issues and limitations](/docs/account?topic=account-known-issues#iam_limits).

## Increasing limits for IAM identity entities
{: #increase-entity-limit}

When your account approaches the maximum limit of one of the entities, you receive a warning in the Activity Tracker event for creating an entity. These events show you the current limits. See the following example:

```text
Nov 26 16:46:01 iamid-6-11-12270-af4d601-cd77fd6bd-86gp7 at.log INFO IAM Identity Service: create account-serviceid 12345678-90ab-cdef-0123-456789abcdef -failure Warning: You have reached 100% of the maximum number of allowed Service IDs in account 11112222333344445555666677778888. Your current count is 3000, and the limit is 3000.
```

A limit increase can be requested for the following types of entities:

* API keys per identity
* Service IDs
* IdPs
* Trusted profiles

You can request a limit increase for the chosen entities only if the following criteria is met:

* You must be the account owner or an administrator on all account management services.
* You have taken efforts to clean up and reduce the number of entities in the account.
* You must have a specific, reasonable use case for requesting an increase. 

### Requesting a limit increase for different entities
{: #request-limit-increase-entity}

If you meet all of the previously listed criteria, you can request a limit increase for the chosen entities by submitting a support case in the [console](/unifiedsupport/cases/add){: external}. In the case, provide all of the following information. Each piece of information is required for the processing and approval of your request. 

* Case title of `Request to increase account <entity> limit`
* The use case for the limit increase
* Information on all efforts taken to reduce the number of `<entities>` on the account
* Account ID
* Note how many extra `<entities>` in the account are required

When the request is approved, the limits for your account are changed.
  
You are notified of the update to your entity limits through the case.
{: note}


## Managing policy limits
{: #policy-limits}

If you aren't sure how many policies are in your account, and you want to ensure that you avoid reaching the limit, you can check how many policies are in your account and work to reduce policies as you approach the limit. You must be the account owner or administrator for all account management services to check how many policies exist in the account.

### Getting the total number of policies per account
{: #total-number-policies}

To get the total number of policies per account, you can use the [IAM Policy Management API](/apidocs/iam-policy-management#get-policies-by-attributes):

1. Log in to {{site.data.keyword.cloud}} CLI. If you have multiple accounts, you are prompted to select which account to use. If you do not specify a region with the `-r` flag, you must also select a region.

   ```bash
   ibmcloud login
   ```
   {: codeblock}

   If your credentials are rejected, you might be using a federated ID. To log in with a federated ID, use the `--sso` flag. See [Logging in with a federated ID](/docs/account?topic=account-federated_id) for more details.
   {: tip}
  
   If it's your first time using the {{site.data.keyword.cloud_notm}} CLI, check out the [getting started tutorial](/docs/cli?topic=cli-getting-started).
  
2. Generate your IAM access token: 

   ```bash
   ibmcloud iam oauth-tokens
   ```
   {: codeblock}
    
3. Enter the following `curl` command to get a total number of policies in one account. You can find the correct value for the `account_id` query parameter by running the `ibmcloud account list` command. The account ID is in the Account GUID column. You might want to install `jq` to format the JSON, which is used in the following examples: 

   ```bash
   curl --location --request GET "https://iam.cloud.ibm.com/v1/policies?account_id=<account_id>" \
       --header "Content-Type: application/json" \
       --header "Authorization: <IAM TOKEN>" | jq -r .policies | jq '. | length'
   ```
   {: codeblock}
    
In the following example output, the last line displays the total number of policies:

   ```bash
    % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                     Dload  Upload   Total   Spent    Left  Speed
   100  2919  100  2919    0     0   3918      0 --:--:-- --:--:-- --:--:--  3912
   351
   ```
   {: codeblock} 

### Getting the total of a specific type of policies per account
{: #total-policies-by-type}

To get the total number of policies for a specific subject, you can use the [IBM Cloud CLI](/docs/cli?topic=cli-getting-started):

Log in, and select your account to run the appropriate CLI command. You might want to install `jq` to format JSON in the CLI output.
  
To get count of policies for a service ID:

```bash
ibmcloud iam service-policies <service-id> -f --output JSON | jq '. | length'
```
{: codeblock}
    
To get count of policies for a username(email):

```bash
ibmcloud iam user-policies <username> -f --output JSON | jq '. | length'
```
{: codeblock}
    
To get count of policies for an access group ID:

 ```bash
ibmcloud iam access-group-policies <access-group> -f --output JSON | jq '. | length'
```
{: codeblock}
    
### Requesting a policy limit increase
{: #limit-increase}

You can request a limit increase for the total number of policies that are allowed in the account only if the following criteria is met: 

* You must be the account owner or an administrator on all account management services.
* Access groups are currently used to limit the overall number of policies in the account.
* Use policies for resources grouped by resource group.
* You have taken efforts to clean up and reduce the number of policies in the account.

If you meet all of the listed criteria, you can request a policy limit increase by submitting a support case in the [console](/unifiedsupport/cases/add){: external}. In the case, provide all of the following information. Each piece of information is required for processing and approval of your request.

* Case title of `Request to increase account policy limit`
* The use case for the extra policies
* Information on all efforts taken to follow the [Best practices for organizing resources and assigning access](/docs/account?topic=account-account_setup#how_access) to reduce the number of policies on the account
* Account ID
* Note how many extra policies in the account are required
* If you are requesting an increase per subject, note how many extra policies per subject are required
* If you are requesting an increase of policies with access management tags, note how many extra policies with access management tags are required
* An estimate of when you expect or plan to create extra policies

You are notified of the update to your policy limits through the case.
{: note}

