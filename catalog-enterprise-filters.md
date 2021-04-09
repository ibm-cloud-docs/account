---

copyright:
  years: 2020, 2021
lastupdated: "2021-04-09"

keywords: catalog, private catalog, catalog management service, public catalog, enterprise account, child account, account group

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:external: target="_blank" .external}

# Customizing the {{site.data.keyword.cloud_notm}} catalog for an enterprise
{: #catalog-enterprise-restrict}

As the account owner or administrator, you can manage which products in the {{site.data.keyword.cloud}} catalog are available for your enterprise. You can choose to include all products, a set of products, or only certain products. You can also specify what level of the enterprise hierarchy the filters apply to. And, you can further restrict which products are available for a specific account group or account. 
{: shortdesc}

## Before you begin
{: #catalog-enterprise-prereqs}

* [Set up your enterprise](/docs/account?topic=account-enterprise-tutorial).
* Make sure you have the [administrator role on the catalog management service](/docs/account?topic=account-account-services#catalog-management-account-management).

## Managing products at the enterprise level
{: #catalog-enterprise-filter}

Centrally manage what's available in the catalog for your entire enterprise hierarchy by setting filters at the enterprise level. The filters automatically apply to all child account groups and accounts. 

Let's say your organization is tasked with implementing a development and deployment model that's focused on improved speed, quality, and control. You might choose to restrict the catalog to only {{site.data.keyword.IBM_notm}} products that are related to DevOps technologies for all members in your enterprise. 

1. In the console, go to **Manage** > **Catalogs** > **Settings**.
2. Select **Exclude all products in the {{site.data.keyword.cloud_notm}} catalog**.
3. Select one or more filters to customize which products are available. In the case of our example, select the following filters: 

  * **Category** > **Developer Tools**
  * **Provider** > **{{site.data.keyword.IBM_notm}}**
4. Review the **Preview** table to confirm your selections, and click **Update**. 
5. Verify your updates in the catalog by going to **Catalog** > **Services**.
6. Expand the list of accounts in the console menu bar and select a child account to verify the catalog includes only the products you selected. 

## Managing products for child account groups and accounts
{: #catalog-enterprise-child}

To build on the example in the previous section, all account groups and accounts in your  enterprise have access to Developer Tools products provided by {{site.data.keyword.IBM_notm}}. You can further restrict access to a subset of products for child account groups and accounts. For example, you might want to limit a specific account group, and its child accounts, to work with only the products that support IAM for access control. 

1. Go to **Manage** > **Catalogs** > **Settings**.
2. Expand the enterprise hierarchy, and select the specific account group. 
3. Select **Exclude all products in the {{site.data.keyword.cloud_notm}} catalog**.
4. Select **Compliance** > **IAM-enabled**. 
5. Review the **Preview** table to confirm your selections, and click **Update**. 
6. Switch to a child account in the account group by selecting it from the list of accounts in console menu bar. 
6. Verify your updates in the catalog by going to **Catalog** > **Services**.
















