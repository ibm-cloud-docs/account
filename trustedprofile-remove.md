---

copyright:

  years: 2021

lastupdated: "2021-10-20"

keywords: trusted profile, federated users, compute resources, granting access, remove trusted profile, IAM trusted profile, trust relationship, establish trust
subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
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

# Removing trusted profiles
{: #trusted-profile-remove}

When you remove trusted profiles, compute resources and federated users are unlinked from the profile and can no longer apply the trusted profile identity.
{: shortdesc}

To remove trusted profiles, you must be assigned the administrator or operator role within the account, or on the IAM Identity Service. 

When you remove trusted profiles, you revoke all active sessions. Users are immediately logged out and the removed profiles are no longer available to connect to the target account. API calls that use access tokens might be successful until the access token expires. 
{: note}

## Removing trusted profiles in the console
{: #remove-tp-console}
{: ui}

1. To see the full list of trusted profiles in your account, go to **Manage** > **Access (IAM)** in the {{site.data.keyword.cloud_notm}} console, and select **Trusted profiles**.
2. Click the **Actions** icon ![Actions icon](../icons/action-menu-icon.svg) next to the trusted profile you want to remove, and select **Remove**.

## Removing trusted profiles by using the CLI
{: #remove-tp-cli}
{: cli}

You can remove a trusted profile from your account by using the CLI. For more information, see the [IBM Cloud CLI](https://github.com/IBM-Cloud/ibm-cloud-cli-release/releases). 

1. Log in, and select the account.

   ```bash
   ibmcloud login
   ```
   {: codeblock}
   
1. Check the list of trusted profiles for the current account and select the one that you want to remove. The following command shows the list of trusted profiles for your {{site.data.keyword.Bluemix_notm}} account:

   ```bash
   ibmcloud iam trusted-profiles
   ```
   {: codeblock}  
   
1. Remove the trusted profile from your account by running the following command. Specify the ID or the name of the trusted profile that you would like to remove.

   ```bash
   ibmcloud iam trusted-profile-delete <IDorName>
   ```
   {: codeblock}
   
For example, the following command removes a trusted profile that is named `Test trusted profile`. 

   ```bash
   ibmcloud iam trusted-profile-delete <Test trusted profile>
   ```
   {: codeblock}
   
## Removing trusted profiles by using the API
{: #remove-tp-api}
{: api}

To remove a trusted profile from your account, call the following:

```bash
curl -X DELETE 'https://iam.cloud.ibm.com/v1/profiles/PROFILE_ID' -H 'Authorization: Bearer TOKEN'
```
{: codeblock}

For more information, see the [IAM Identity Services API](/apidocs/iam-identity-token-api). 
