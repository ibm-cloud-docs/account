---

copyright:
  years: 2020
lastupdated: "2020-04-02"

keywords: catalog, visibility, filter catalog, hide product, catalog filtering, validating

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:new_window: target="_blank"}

# Validating filters set at the account level
{: #validate-acctfilter}

In this tutorial, you validate that you can view all {{site.data.keyword.IBM}} products, except for {{site.data.keyword.appid_short_notm}}, in the {{site.data.keyword.cloud}} catalog.
{: shortdesc}

## Before you begin
{: #prereqs-acctfilter-validate}

To complete this tutorial, you need to be assigned only the viewer role on the catalog management service. With this type of access, you can view only the products included in the filter that the administrator set in [Customizing the {{site.data.keyword.cloud_notm}} catalog for all account users](/docs/account?topic=account-filter-account). You can also view what filters the administrator set, but you can't update them. For more information, see [Assigning users access](/docs/account?topic=account-catalog-access).

  If you don't see what you're expecting in the console based on your permissions, try refreshing your session by going to https://cloud.ibm.com/login.
  {: tip}

## Validate the filtered catalog view 
{: #validate-steps}

Complete the following steps to validate that {{site.data.keyword.appid_short_notm}} is not included in the catalog.

1. Click **Catalog** in the console menu bar.
1. Search for {{site.data.keyword.appid_short_notm}}, and confirm that no results are returned. The product is not available, because the administrator set a filter to exclude it from the catalog. 
1. Go to **Manage** > **Catalogs** > **Settings**. Confirm that you can view the current settings, but you can't update them.

### Success criteria
{: #console-success-acctfiltervalidate}

As a viewer, you successfully completed this task if the following items are true:

* No results are returned when you search the catalog for {{site.data.keyword.appid_short_notm}}.
* You can view details on the Settings page, but you can't update them. 

## Next steps
{: #next-filter-private}

A user with access to a private catalog sets a filter to include only specific {{site.data.keyword.IBM_notm}} products. See [Customzing your private catalogs](/docs/account?topic=account-restrict-by-user) for more information.
