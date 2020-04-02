---

copyright:
  years: 2020
lastupdated: "2020-04-02"

keywords: catalog, restrict offering, hide offering, restrict by user

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:new_window: target="_blank"}

# Validating filters set at the private catalog level
{: #restrict-user-validate}

In this tutorial, you validate that you can view specific {{site.data.keyword.IBM}} products in the private catalog you've been given access to. 
{: shortdesc}

## Before you begin
{: #prereq-restrict-validate}

To complete this tutorial, you need to be assigned the viewer role on the private catalog service. With this type of access, you can view only the offerings included in the filter that the private catalog editor previously set. You can also view what filters the editor set, but you can't update them. For more information, see [Assigning users access](/docs/account?topic=account-catalog-access).

  If you don't see what you're expecting in the console based on your permissions, try refreshing your session by going to https://cloud.ibm.com/login.
  {: tip}

## Validate your filtered view in the console 
{: #restrict-filter-validate}

Validate that your private catalog includes Cloudant and Kubernetes Service:

1. Click **Catalog** in the console menu bar. 
2. Select **My first catalog** from the list of catalogs.
1. Search for Cloudant and Kubernetes Service, and confirm that the products are included in the search results. 
<br>  

Next, validate that you can't edit the applied filters:

1. Go to [Manage > Catalogs](https://cloud.ibm.com/content-mgmt/catalogs), and select **Settings**. Confirm that you can view the current settings, but you can't update them.
1. Click **Private catalogs** > **My first catalog**.
1. Click **{{site.data.keyword.IBM_notm}} offerings** > **Manage filters**. Confirm that you can view the current settings, but you can't update them. 

### Success criteria
{: #restrict-success-filter}

As a viewer, you successfully completed this task if the following items are true:

* You can find Cloudant and Kubernetes Service in the {{site.data.keyword.cloud_notm}} catalog.
* You can't update the filters on the Settings page or on the Manage filters page within the `My first catalog` private catalog.

## Validate your filtered view by using the CLI
{: #restrict-validate-cli} 

Run the following command to validate that you can view Cloudant and Kubernetes Service in your private catalog:

  ```
  ibmcloud catalog offering list --catalog "My first catalog"
  ```
  {: codeblock}

### Success criteria
{: #restrict-success-cli}

You successfully completed this task if you ran the command and the specific products were included in the output. 

## Next steps
{: #next-addsw}

A user creates a private catalog and adds their own software offering to it. See [Adding your software to a private catalog](/docs/account?topic=account-create-private-catalog) for more information.


