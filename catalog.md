---

copyright:
  years: 2017, 2020
lastupdated: "2020-04-02"

keywords: catalog, restrict offerings, public catalog, private catalog, Helm chart, Terraform, add software

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:new_window: target="_blank"}

# Working with the {{site.data.keyword.cloud_notm}} catalog and your private catalogs
{: #manage-catalog}

Learn how to manage the {{site.data.keyword.cloud}} offerings that users can view in the {{site.data.keyword.cloud_notm}} catalog and in the private catalogs they have access to. Gain an understanding of how to add your own offerings to private catalogs to make them available for users with the required access. 
{: shortdesc}

## Before you begin
{: #landing-prereqs}

### Assign users access
{: #access-prereq}

The account owner must assign users in their account specific access roles so they can successfully complete the tutorials. For more information, see [Assigning users access](/docs/account?topic=account-catalog-access).

### Install the CLI and plug-in
{: #cli-plugin-install}

You can complete the tutorials by using either the {{site.data.keyword.cloud_notm}} console or command-line interface (CLI). Make sure you install the {{site.data.keyword.cloud_notm}} CLI and the catalogs management CLI plug-in. For details about installing the CLI, see [Getting started with the {{site.data.keyword.cloud_notm}} CLI and Developer Tools](/docs/cli?topic=cloud-cli-getting-started).

After you install the {{site.data.keyword.cloud_notm}} CLI, log in with the **`ibmcloud login`** command to generate an access token and authenticate your session. Then, run the following command to install the catalogs management CLI plug-in:

  ```
  ibmcloud plugin install catalogs-management
  ```
  {: codeblock}

You can run the following command to verify that the CLI plug-in is installed:

  ```
  ibmcloud plugin list | grep catalogs
  ```
  {: codeblock}
  
## Walking through the tutorials
{: catalogs-get-started}

The catalog management tutorials walk you through the steps for restricting the type of offerings, services and software, that users can access from the {{site.data.keyword.cloud_notm}} catalog. You can learn how to tailor the list of available offerings for different groups of users in your account. Also, you can add Helm charts or Terraform-based software offerings to your account for users to consume. 

  * [Filtering the {{site.data.keyword.cloud_notm}} catalog for all account users](/docs/account?topic=account-filter-account): Set filters to include or exclude specific offerings from the {{site.data.keyword.cloud_notm}} catalog. These filters apply to all users in your account.
  * [Filtering the {{site.data.keyword.cloud_notm}} catalog at a private catalog level](/docs/account?topic=account-restrict-by-user): Create a private catalog, and set an additional filter that further scopes the catalog to users with access to your private catalog. 
  * [Adding your software to a private catalog](/docs/account?topic=account-create-private-catalog): Add your own software offering to your private catalog.
  * [Installing a private software offering](/docs/account?topic=account-install-sw): Install the software offering from your private catalog.
  * [Updating a software offering](https://test.cloud.ibm.com/docs/account?topic=account-update-private): Update the readme of the current version of your software offering, and add a new version of your offering.
  * [Deprecating and restoring a version of a software offering](https://test.cloud.ibm.com/docs/account?topic=account-dep-restore): Deprecate and then restore a specific version of your software offering.






