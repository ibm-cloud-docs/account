---

copyright:
  years: 2020, 2022
lastupdated: "2022-06-14"

keywords: secrets manager

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Using a secret from Secrets Manager
{: #using-secret}

{{site.data.keyword.secrets-manager_short}} is a beta service that is available for evaluation and testing. Beta services might be unstable or change frequently.
{: beta}

You can use {{site.data.keyword.secrets-manager_full_notm}} to create a secret that can be used in place of an access token, API key, password, or any type of credential that you might use to access a confidential system. Instead of giving the user the Personal access token for a private repository, you can give the user access to the secret and add the token to a secret and centrally manage all tokens and access the secret allows. For more information, see [Getting started with Secrets Manager](/docs/secrets-manager?topic=secrets-manager-getting-started). 
{: shortdesc} 

## Before you begin
{: #prereq-secret}

You need to have a private catalog created. 

To use a secret, you need the writer service role for Secrets Manager. For more information, see [Managing access for Secrets Manager](/docs/secrets-manager?topic=secrets-manager-iam). 

If you're onboarding an offering to your private catalog, you need to have additional access for [integrating with other services](/docs/secrets-manager?topic=secrets-manager-integrations). 
{: important}


## Onboard your product by using a secret
{: #onboard-use-secret}

To use a secret, you need to add a product to a private catalog from a private repository. Complete the following steps to use a secret to add a product from a private repository. 

1. Go to **Manage** > **Catalogs** > **Private catalogs** in the {{site.data.keyword.cloud_notm}} console.
1. Select your private catalog and select **Private products**. 
1. Click **Add**. 
1. Select the **Private repository**. 
1. Select **Yes** to use a secret and click **Select from Secrets Manager**. 
1. To select a secret, you need to drill down the choices to find the relevant secret. Select a **Service instance**. Select a **Secret group**. Select a **Secret**. If you don't see your secret, make sure you're using the correct secret group and service instance. 

Service instance will display `No service instance available` if you don't have secrets created or if you don't have the correct access to use secrets, even if you have service instances created. 
{: note}
