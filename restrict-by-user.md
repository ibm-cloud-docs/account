---

copyright:
  years: 2020
lastupdated: "2020-02-05"

keywords: catalog, restrict visibility, hide offering, restrict by user, filter catalog

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:new_window: target="_blank"}

# Filtering the {{site.data.keyword.cloud_notm}} catalog at a private catalog level
{: #restrict-by-user}

In this tutorial, you set a filter to restrict users from viewing offerings that provide free pricing plans in the {{site.data.keyword.cloud}} catalog.  
{: shortdesc}

This feature is available only in a closed beta. If you’re interested in participating, contact kala.nenkova@ibm.com.
{: note}

## Before you begin
{: #prereq-restrict}

To complete this tutorial, you need to be assigned only the editor role on the private catalog service. With this type of access, you can create private catalogs and set filters that apply only to users with access to your private catalog. You can also view the account-level filters on the Settings page, but you can't edit them. For more information, see [Assigning users access](/docs/account?topic=account-catalog-access).

  If you don't see what you're expecting in the console based on your permissions, try refreshing your session by going to https://cloud.ibm.com/login.
  {: tip}

## Create a private catalog and set a filter in the console
{: #restrict-editor-filter}

Complete the following steps to create your private catalog and set a filter that excludes offerings with free plans from the {{site.data.keyword.cloud_notm}} catalog.

1. Go to [Manage > Catalogs](https://cloud.ibm.com/content-mgmt/catalogs), and click **Create**.
1. Enter `My first catalog` as the catalog name, select the resource group that you want to assign it to, and click **Create**.
2. Click the name of your new catalog.
1. Click **{{site.data.keyword.cloud_notm}} catalog**. The list that's displayed includes the available offerings based on the filter that the administrator set on the Settings page. 
2. Click **Manage filters** to set additional restrictions that apply only to users with access to the private catalog that you're creating. 
3. In the Rules section, click the **Edit** icon ![Edit icon](../icons/edit-tagging.svg).
4. Make sure **Including all offerings in the {{site.data.keyword.cloud_notm}} catalog** is selected, and click **Add rule**.
5. Select **Pricing plan** from the list, and click **Free**. 
6. Click **Update**.

## Create a private catalog and set a filter by using the CLI
{: #restrict-cli-filtering}

Complete the following steps to create your private catalog and set a filter that excludes offerings with free plans from the {{site.data.keyword.cloud_notm}} catalog.

1. If you created the `My first catalog` catalog in the previous section, delete it.
    
    ```
    ibmcloud catalog delete --catalog "My first catalog"
    ```
    {:codeblock}
    
1. Create a new private catalog in your account.

  You must target a resource group to create a catalog, as the catalog exists in the context of a particular resource group. To get a list of the resource groups in the account, run the `ibmcloud resource groups` command and then the `ibmcloud target -g "resource group"` command.
  {: important}
    
    ```
    ibmcloud catalog create --name "My first catalog" --description "A private catalog for testing purposes"
    ```
    {:codeblock}
    
1. Create a filter that excludes offerings with free plans from the {{site.data.keyword.cloud}} catalog. This filtered view applies to all users with access to your private catalog.
    
    ```
    ibmcloud catalog filter create --catalog "My first catalog" --include-all true  --pricing-plan free
    ```
    {:codeblock}

## Next steps
{: #next-restrictuser}

A user with access to the private catalog validates that they can't view offerings with free pricing plans in the {{site.data.keyword.cloud}} catalog. See [Validating filters set at the private catalog level](/docs/account?topic=account-restrict-user-validate) for more information.


