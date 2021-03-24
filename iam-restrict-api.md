---

copyright:

  years: 2020, 2021

lastupdated: "2021-03-24"

keywords: restrict api keys, block users from creating api keys, restrict api key creation

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}

# Restricting users from creating API keys
{: #allow-api-create}

By default, all members of an account can create {{site.data.keyword.cloud}} API keys. However, that access can be restricted so that only members with the correct access can create these user API keys by using the API key creation setting. Restricting the ability to create API keys makes sense if you want users in your account to always log in interactively, meaning you don't want automation scripts to run that can log in users automatically by using an API key. For more information about API keys, see [Managing user API keys](/docs/account?topic=account-userapikey).  
{:shortdesc}


## Enabling the API key creation setting
{: #allow-all-api-create}

To turn on the setting to restrict users from creating user API keys, you must have the following assigned access:

* An IAM policy with the `Administrator`, `Operator`, or `Editor` role on the [IAM Identity Service](/docs/account?topic=account-account-services#identity-service-account-management).

If you turn on the API key creation setting, users in your account require specific access to create API keys, including the account owner. To restrict who can create API keys, use the following steps:

Enabling this setting affects only the creation of user API keys. It does not affect API keys for service IDs.
{: note}

1. In the {{site.data.keyword.cloud_notm}} console, go to **Manage** > **Access (IAM)**, and select **Settings**.
2. In the Account restrictions section, turn on the **API key creation** setting.

Now that the setting is enabled to restrict users from creating API keys, you can assign the required access to enable specific users to continue creating user API keys. Remember, the account owner is also required to be assigned this explicit access.
{: important}

## Assigning access to create API keys with restrictions enabled
{: #restrict-api-create-access}

If the API key creation setting is turned on, only users, including the account owner, assigned the `User API key creator` role on the IAM Identity Service can create API keys. 

The quickest way to assign a group of users the required access for creating API keys is to create an access group and assign the group the required role. For more information about assigning access policies, see [Setting up access groups](/docs/account?topic=account-groups).
{: tip}
