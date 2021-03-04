---

copyright:
  years: 2020, 2021
lastupdated: "2021-03-04"

keywords: maximum limits, limits, maximum policies, check for limits, check policy number, increase policy limit, total number of account policies

subcollection: account

---


{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}

# Managing policy limits
{: #policy-limits}

If you aren't sure how many policies are in your account, and you want to ensure that you avoid reaching the limit, you can check how many policies are in your account and work to reduce policies as you approach the limit. You must be the account owner or administrator for all account management services to check how many policies exist in the account.
{: shortdesc}

## Getting the total number of policies per account
{:# total-number-policies}

To get the total number of policies per account, you can use the [IAM Policy Management API](/apidocs/iam-policy-management#get-policies-by-attributes):

1. Log in to {{site.data.keyword.cloud}} CLI. If you have multiple accounts, you are prompted to select which account to use. If you do not specify a region with the `-r` flag, you must also select a region.
  ```
  ibmcloud login
  ```
  {: codeblock}

  If your credentials are rejected, you might be using a federated ID. To log in with a federated ID, use the `--sso` flag. See [Logging in with a federated ID](/docs/account?topic=account-federated_id) for more details.
  {: tip}
  
  If it's your first time using the {{site.data.keyword.cloud_notm}} CLI, check out the [getting started tutorial](/docs/cli?topic=cli-getting-started).
  
2. Generate your IAM access token: 
    ```
    ibmcloud iam oauth-tokens
    ```
    {: codeblock}
    
3. Enter the following `curl` command to get a total number of policies in one account. You can find the correct value for the `account_id` query parameter by running the `ibmcloud account list` command. The account ID is in the Account GUID column. You might want to install `jq` to format the JSON, which is used in the following examples: 
    ```
    curl --location --request GET "https://iam.cloud.ibm.com/v1/policies?account_id=<account_id>" \
       --header "Content-Type: application/json" \
       --header "Authorization: <IAM TOKEN>" | jq -r .policies | jq '. | length'
    ```
    {: codeblock} 
In the following example output the last line displays the total number of policies:
    ```
      % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                     Dload  Upload   Total   Spent    Left  Speed
      100  2919  100  2919    0     0   3918      0 --:--:-- --:--:-- --:--:--  3912
      351
    ```
    

## Getting the total of a specific type of policies per account
{: #total-policies-by-type}

To get the total number of policies for a specific subject, you can use the [IBM Cloud CLI](/docs/cli?topic=cli-getting-started):

Log in, and select your account to run the appropiate CLI command. You might want to install `jq` to format JSON in the CLI output.
  
* To get count of policies for a service id:
    ```
       ibmcloud iam service-policies <service-id> -f --output JSON | jq '. | length'
    ```
    {: codeblock}
    
* To get count of policies for a username(email):
    ```
       ibmcloud iam user-policies <username> -f --output JSON | jq '. | length'
    ```
    {: codeblock}
    
* To get count of policies for an access group id:
    ```
       ibmcloud iam access-group-policies <access-group> -f --output JSON | jq '. | length'
    ```
    {: codeblock}

## Requesting a policy limit increase
{: #limit-increase}

You can request a limit increase for the total number of policies that are allowed in the account only if the following criteria is met: 

* You must be the account owner or an administrator on all account management services.
* Access groups are currently used to limit the overall number of policies in the account.
* Use policies for resources grouped by resource group.
* You have taken efforts to clean up and reduce the number of policies in the account.

If you meet all of the listed criteria, you can request a policy limit increase by submitting a support case in the [console](https://{DomainName}/unifiedsupport/cases/add){: external}. In the case, provide all of the following information. Each piece of information is required for processing and approval of your request.

* Case title of `Request to increase account policy limit`
* The use case for the extra policies
* Information on all efforts taken to follow the [Best practices for organizing resources and assigning access](/docs/account?topic=account-account_setup#how_access) to reduce the number of policies on the account
* Account ID
* Note how many extra policies in the account are required
* If you are requesting an increase per subject, note how many extra policies per subject are required
* An estimate of when you expect or plan to create extra policies

You are notified of the update to your policy limits through the case.
{: note}

