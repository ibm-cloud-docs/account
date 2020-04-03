---

copyright:
  years: 2019, 2020
lastupdated: "2020-04-02"

keywords: catalog, private catalogs, visibility, filter catalog, hide product, catalog filtering

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:external: target="_blank" .external}

# Customizing the {{site.data.keyword.cloud_notm}} catalog for all account users
{: #filter-account}

This tutorial walks you through the steps to customize the {{site.data.keyword.cloud_notm}} catalog by setting a filter to include all {{site.data.keyword.IBM}} products, except for {{site.data.keyword.appid_full}}.
{: shortdesc}

## Before you begin
{: #prereqs-acctfilter}

To complete this tutorial, you need to be assigned the administrator role on the catalog management service. With this type of access, you can set filters in the {{site.data.keyword.cloud_notm}} catalog for all users in the account. For more information, see [Assigning users access](/docs/account?topic=account-catalog-access).

  If you don't see what you're expecting in the console based on your permissions, try refreshing your session by going to https://cloud.ibm.com/login.
  {: tip} 

## Set a catalog filter by using the console
{: #create-acctfilter}

Complete the following steps to set a filter that includes all {{site.data.keyword.cloud_notm}} products in the catalog except for {{site.data.keyword.appid_short_notm}}.

1. Log in to your account, and go to **Manage** > **Catalogs** > **Settings**.
2. Make sure the visibility of the {{site.data.keyword.cloud_notm}} catalog is turned on.
1. In the Rules section, click the **Edit** icon ![Edit icon](../icons/edit-tagging.svg).
1. Select **Exclude all products in the {{site.data.keyword.cloud_notm}} catalog** to start with an empty catalog.   
1. Click **Add rule**, select **Provider**, and click **IBM**. 
1. Click **Add exception**, and select **Exclude** > **{{site.data.keyword.appid_short_notm}}**.
1. In the Preview section, verify that the value for {{site.data.keyword.appid_short_notm}} in the Included column is No. 
1. Click **Update** to apply your changes. 

## Set a catalog filter by using the CLI 
{: #cli-acctfilter}

Before you begin, make sure you [install the {{site.data.keyword.cloud_notm}} CLI and the catalogs management CLI plug-in](/docs/account?topic=account-manage-catalog#landing-prereqs).
<br>

1. Remove the existing filter that you created in the previous steps.
    ```
    ibmcloud catalog filter delete
    ```
    {: codeblock}
    
1. Create a filter that includes all {{site.data.keyword.IBM_notm}} products in the catalog, except for {{site.data.keyword.appid_short_notm}}.
    ```
    ibmcloud catalog filter create --include-all false --provider ibm_created --exclude-list appid
    ```
    {: codeblock}

## Next steps
{: #next-acctfilter}

A user in the account validates that they can't view {{site.data.keyword.appid_short_notm}} in the catalog. See [Validating the account-level catalog filters](/docs/account?topic=account-validate-acctfilter) for more information.


