---

copyright:
  years: 2020
lastupdated: "2020-06-12"

keywords: catalog, restrict visibility, hide product, restrict by user, filter catalog, private catalog, catalog management service, public catalog

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:external: target="_blank" .external}

# Customizing your private catalogs
{: #restrict-by-user}

Private catalogs provide a way to centrally manage access to products in the {{site.data.keyword.cloud}} catalog and your own catalogs. You can customize your private catalogs to make specific solutions available to your users. By doing so, you can ensure that your catalogs are relevant to your business. 
{: shortdesc}

Let's say you're an operations admin for your team, and you require access to all products in the {{site.data.keyword.cloud_notm}} catalog. A member of your team is tasked with a specific project, for example, building a voice-enabled chatbot by using {{site.data.keyword.conversationshort}}, {{site.data.keyword.speechtotextshort}}, and {{site.data.keyword.texttospeechshort}}. And, you want them to access only those products in the {{site.data.keyword.cloud_notm}} catalog.  

To achieve this, you create one catalog that includes all products in the {{site.data.keyword.cloud}} catalog. Then, you create another catalog that includes only the required products, and you give the team member viewer access to the catalog. 

All private catalogs that are in an account inherit filters that are set by the account owner or administrator at the account level. In addition, if the account is a parent account in an {{site.data.keyword.cloud_notm}} enterprise, the filters apply to all child account groups and accounts.
{: tip}

## Before you begin
{: #prereq-restrict}

* To complete this task, you need the administrator role on the catalog management service. See [Assigning access to account management services](/docs/iam?topic=iam-account-services) for more information. 
* To give users access to your private catalog, invite them to join your {{site.data.keyword.cloud_notm}} account. See [Inviting users to an account](/docs/iam?topic=iam-iamuserinv) for more information.

## Creating a private catalog with all products
{: #catalog-all}

Complete the following steps to create a catalog that includes all products in the {{site.data.keyword.cloud_notm}} catalog:

1. In the console, go to **Manage** > **Catalogs**, and click **Create a catalog**.
1. Enter a name, make sure the **Start with all available products in this account** option is selected, and click **Create**. 

  As the account owner or administrator, you control which products are available by setting filters from the Settings page. Any filters that you set at the account level are inherited by all private catalogs that are in your account. 
  {: tip}
  
2. Confirm that the catalog includes all products by clicking the catalog name > **Manage filters**. Then, check that **Include all products in the {{site.data.keyword.cloud_notm}} catalog** is selected in **Step 1: Select to include or exclude all products in the {{site.data.keyword.cloud_notm}} catalog**.

## Creating a private catalog with select products
{: #catalog-select}

Complete the following steps to create a catalog that includes a specific set of products in the {{site.data.keyword.cloud_notm}} catalog:

1. Go to **Manage** > **Catalogs**, and click **Create a catalog**.
2. Enter a name, and click **Create**.
3. Click the catalog name > **Manage filters**.
4. Select **Exclude all products in the {{site.data.keyword.cloud_notm}} catalog** in **Step 1: Select to include or exclude all products in the {{site.data.keyword.cloud_notm}} catalog**. 
5. Skip step 2, and click **Add** in **Step 3: Add exceptions to the rules**. 
6. Make sure **Include** is selected as the condition, and then individually select the products you want users to access. In the case of our example project, you select {{site.data.keyword.conversationshort}}, {{site.data.keyword.speechtotextshort}}, and {{site.data.keyword.texttospeechshort}}.

## Setting the visibility of the {{site.data.keyword.cloud_notm}} catalog
{: #catalog-off}

Now that you created your private catalogs, complete the following steps to turn off visibility of the public catalog to all users in your account.

1. Click **Catalogs** in the breadcrumb at the top of the page.
2. Click **Settings**.
3. Set **{{site.data.keyword.cloud_notm}} catalog** to **Off**. 
4. Confirm that your filters and settings are correctly applied by going to the public catalog, and expanding the catalog switcher. Only the private catalogs in your account should be displayed in the list. 

## Authorizing access to private catalogs
{: #customcatalog-access}

To authorize users to work with the products in your private catalogs, assign them the viewer role for the specific catalog. See [Assigning access to account management services](/docs/iam?topic=iam-account-services) for more information.  












