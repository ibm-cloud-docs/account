---

copyright:
  years: 2019, 2020
lastupdated: "2020-10-06"

keywords: catalog, catalogs, private catalogs, account catalogs, catalog visibility, software visibility, import software

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:external: target="_blank" .external}
{:beta: .beta}

# Adding your software to a private catalog
{: #create-private-catalog}

You can add products to a private catalog to centrally manage all usable services within your account. You can onboard your software by using a public or private repository. If you choose to onboard with a private repository, you can use a personal access token for verification or you can use a [secret](/docs/secrets-manager?topic=secrets-manager-secret-basics). 
{: shortdesc} 

## Before you begin
{: #prereq-create}

* You need a [Kubernetes cluster](https://cloud.ibm.com/kubernetes/landing){: external} to validate your software.
* You need to be assigned the following roles:
  * Editor role on the catalog management service
  * Writer role on the {{site.data.keyword.secrets-manager_short}} service
  * Viewer role on all resource groups. Select **No service access**, a resource group name, then the role, and repeat for each resource group.
  For more information, see [Assigning users access](/docs/account?topic=account-catalog-access).

  If you're using a secret to onboard an offering from a private repository, you need to have additional access for [integrating with other services](/docs/secrets-manager?topic=secrets-manager-integrations). 
  {: important}


## Creating a private catalog
{: #create-private-catalog}

Before you can add an offering to a private catalog, you first need to create a private catalog. To create a private catalog, use the following steps:

1. Go to **Manage** > **Catalogs** > **Private catalogs**. 
1. Click **Create** to start creating a new private catalog.
1. Enter the catalog name and choose whether you want to start with an empty catalog or with available products included, and click **Create**.

## Adding software from a public repository
{: #add-public-repo}

You can add your product from a public or private repository. To add from a public repository, use the following steps:

1. Go to **Manage** > **Catalogs** > **Private catalogs**.
1. Select your private catalog and select **Private products**. 
1. Click **Add**. 
1. Enter your repository's URL or TGZ archive. 
1. Select the Category and Deployment target. 
1. Click **Add**.  

## Adding software from a private repository
{: #add-private-repo}

You can add your product from a public or private repository. When you use a private repository, you need to provide a personal access token or you can use a secret. 

### Using a personal access token
{: #add-software-token}

To add from a private repository by using a personal access token, use the following steps:

1. Go to **Manage** > **Catalogs** > **Private catalogs**.
1. Select your private catalog and select **Private products**. 
1. Click **Add**. 
1. Select the **Private repository**. 
1. Select **No** for using a secret and provide your personal access token for your private repository. Or you can [use a secret]
1. Select the Category and Deployment target.
1. Click **Add**. 

### Using a secret
{: #add-use-secret}

{{site.data.keyword.secrets-manager_short}} is a beta service that is available for evaluation and testing. Beta services might be unstable or change frequently.
{: beta}

You can use {{site.data.keyword.secrets-manager_full_notm}} to create a secret that can be used in place of an access token, API key, password, or any type of credential that you might use to access a confidential system. Instead of giving the user the Personal access token for a private repository, you can give the user access to the secret and add the token to a secret and centrally manage all tokens and access the secret allows. For more information, see [Getting started with Secrets Manager](/docs/secrets-manager?topic=secrets-manager-getting-started). 
{: shortdesc} 

To use a secret, you need the writer service role for Secrets Manager. For more information, see [Managing access for Secrets Manager](/docs/secrets-manager?topic=secrets-manager-iam). 

If you're onboarding an offering to your private catalog, you need to have additional access for [integrating with other services](/docs/secrets-manager?topic=secrets-manager-integrations). 
{: important}

Complete the following steps to use a secret:

1. Go to **Manage** > **Catalogs** > **Private catalogs**.
1. Select your private catalog and select **Private products**. 
1. Click **Add**. 
1. Select the **Private repository**. 
1. Select **Yes** to use a secret and click **Select from Secrets Manager**. 
1. To select a secret, you need to drill down the choices to find the relevant secret. Select a **Service instance**. Select a **Secret group**. Select a **Secret**. If you don't see your secret, make sure you're using the correct secret group and service instance. 
  Service instance displays `No service instance available` if you haven't created a secret or if you don't have the correct access to use secrets, even if you have service instances that are created. 
  {: note}
1. Select the Category and Deployment target. 
1. Click **Add**. 


## Publishing your software to your account
{: #validating-software}

When you publish your software to your account, you make it available for use by each user in that account. Before you can publish to your account, you need to review your software's version details and readme and then validate your software. After you verify your products information, use the following steps to validate:

1. Select **Validate product**. 
1. Select a cluster. 
1. Click **Validate** to ensure that your software can be installed successfully. This step is required before you can make it available for users in your account. This action can take several minutes. In the Validation summary section, the status is displayed as Validated when the deployment is complete. 
1. After you validate your software, you can click the **Actions** icon ![Actions icon](../icons/actions-icon-vertical.svg), and select **Publish to account** to make your software available to all users in your account through your private catalog.


## Add your software by using the CLI
{: #create-cicd-product}

Complete the following steps to add your software by using the CLI. You can use this task in a CI/CD process.
    
1. Add software to your private catalog.  
    ```
    ibmcloud catalog offering create --catalog "Name of catalog" --zipurl https://software.url.com.tgz
    ```
    {: codeblock}
    
1. Add the **Developer Tools** category.  
    ```
    ibmcloud catalog offering add-category --catalog "Name of catalog" --offering "software-offering" --category "Developer Tools"
    ```
    {: codeblock}
    
1. Validate the software.  
    
    You need the version locator for your software. To find it, run the **`ibmcloud catalog offering list --catalog "Name of catalog"`** command, and search for the particular version of your software. Also, use the cluster that you created when you set up the required resources. 
    {: important}
    
    ```
    ibmcloud catalog offering validate --version-locator <LOCATOR> --cluster <CLUSTER> --namespace "software-offering"
    ```
    {: codeblock}
    
    Deploying the software can take a few minutes. You can check the validation status by querying the product validation state. The validation is complete when the state is Valid. 
    ```
    ibmcloud catalog offering validate-status --version-locator <LOCATOR>
    ```
    {: codeblock}
    
1. Publish your software to make it available to users in your account. 
    ```
    ibmcloud catalog offering publish-to-account --version-locator <LOCATOR>
    ```
    {: codeblock}
    
## Next steps
{: #install-sw-next}

A user installs the software from your private catalog. See [Installing software from your private catalog](/docs/account?topic=account-install-sw) for more information.
