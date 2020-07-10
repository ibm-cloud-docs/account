---

copyright:
  years: 2019, 2020
lastupdated: "2020-07-10"

keywords: catalog, private catalogs, visibility, filter catalog, hide product, catalog filtering, enterprise, account group, child account, account, restrict

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:external: target="_blank" .external}

# Managing catalog settings
{: #filter-account}

As the account owner or administrator, you can manage the settings for all catalogs across your account. Management tasks include setting the visibility of the {{site.data.keyword.cloud}} catalog and controlling access to products in the public catalog and private catalogs for users in your account.
{: shortdesc}

You need the [administrator role on the catalog management service](/docs/account?topic=account-account-services#catalog-management-account-management) to perform these tasks.

## Updating the visibility of the {{site.data.keyword.cloud_notm}} catalog
{: #set-public-visibility}

Users in your account have access to all products in the public catalog by default. To update what products are visible to users, go to **Manage** > **Catalogs** > **Settings** in the {{site.data.keyword.cloud_notm}} console. 

If you don't have any private catalogs in your account and you turn off the visibility of the public catalog, users can't create instances of any products. Be sure to [create a private catalog](/docs/account?topic=account-restrict-by-user) before you update this setting. 
{: note}

## Managing access to products for all users
{: #set-account-filters}

You can use filters to manage which products in the public catalog are available to all users in your account. For example, you might want to restrict access to third-party products. Or, you might want users to work with a specific software type. 

If your account is a parent account in an {{site.data.keyword.cloud_notm}} enterprise, the filters that you set apply to all child account groups and accounts. For more information, see [Managing products for an an {{site.data.keyword.cloud_notm}} enterprise](/docs/account?topic=account-catalog-enterprise-restrict).
{: tip}

1. In the console, go to **Manage** > **Catalogs** > **Settings**. 
2. Confirm that the visibility of the public catalog is set to **On**.
3. In the What products are available? section, select **Exclude all products in the {{site.data.keyword.cloud_notm}} catalog**.
4. Set one or more filters to customize what products are available by category.
5. (Optional) Add exceptions to the filter rules that you set in the previous step. 
6. Use the **Preview** table to confirm your selections, and click **Update**.

## Managing access to products for specific users 
{: #set-private-filters}

Set filters at a private catalog level for fine-grained control of which products in the public catalog are available only to the users you choose.   

1. In the console, go to **Manage** > **Catalogs**, **Private catalogs**. 
2. Select a catalog from the list to navigate to its details page. 

  The **Products in the {{site.data.keyword.cloud_notm}} catalog** table that's displayed on the page shows the list of products that are available at the account level. The availability is based on the filters the account owner or administator set. Account-level filters apply to all the private catalogs in the account. 
  {: tip}
  
3. Click **Manage filters**.
3. Select to include or exclude all products in the public catalog. 
4. Set one or more filters to customize what products are available by category. 
5. (Optional) Add exceptions to the filter rules that you set in the previous step. 
6. Click **Update**. 
7. Go to the Settings page and turn off the visibility of the public catalog.  
7. To give users access to work with the products in the private catalog, assign them the [viewer role on the catalog management service](/docs/account?topic=account-account-services#catalog-management-account-management).  
<br>
<br>
For more detailed examples of how you can leverage filtering at the private catalog level, see [Customizing your private catalogs](/docs/account?topic=account-restrict-by-user).




 



