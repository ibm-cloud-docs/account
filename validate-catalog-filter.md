---

copyright:
  years: 2020
lastupdated: "2020-02-05"

keywords: catalog, visibility, filter catalog, hide offering, catalog filtering, validating

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:new_window: target="_blank"}

# Validating the account-level catalog filters 
{: #validate-acctfilter}

In this tutorial, you validate that you can view all {{site.data.keyword.cloud}} catalog offerings except {{site.data.keyword.appid_short_notm}}. 
{: shortdesc}

This feature is available only in a closed beta. If you’re interested in participating, contact kala.nenkova@ibm.com.
{: note}

## Before you begin
{: #prereqs-acctfilter-validate}

To complete this tutorial, you need to be assigned only the viewer role on the private catalog service. With this type of access, you can view only the offerings included in the filter that the administrator set in [Filtering the {{site.data.keyword.cloud_notm}} catalog for all account users](/docs/account?topic=account-filter-account). You can also view what filters the administrator set, but you can't update them. For more information, see [Assigning users access](/docs/account?topic=account-catalog-access).

  If you don't see what you're expecting in the console based on your permissions, try refreshing your session by going to https://cloud.ibm.com/login.
  {: tip}

## Validate the filtered catalog view 
{: #validate-steps}

Complete the following steps to validate that {{site.data.keyword.appid_short_notm}} is not included in the catalog.

1. Click **Catalog** in the console menu bar.
1. Search for {{site.data.keyword.appid_short_notm}}, and confirm that no results are returned. The offering is not available, because the administrator set a filter to exclude it from the catalog. 
1. Go to [Manage > Catalogs](https://cloud.ibm.com/content-mgmt/catalogs), and select **Settings**. Confirm that you can view the current setting, but you can't update them.

### Success criteria
{: #console-success-acctfiltervalidate}

As a viewer, you successfully completed this task if the following items are true:

* No results are returned when you search the catalog for {{site.data.keyword.appid_short_notm}}.
* You can view details on the Settings page, but you can't update them. 

## Next steps
{: #next-filter-private}

A user with access to a private catalog sets a filter to restrict users from viewing {{site.data.keyword.cloud_notm}} offerings that provide free pricing plans. See [Filtering the {{site.data.keyword.cloud_notm}} catalog at a private catalog level](/docs/account?topic=account-restrict-by-user) for more information.
