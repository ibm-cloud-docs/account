---

copyright:
  years: 2019, 2020
lastupdated: "2020-02-12"

keywords: catalog, private catalogs, visibility, filter catalog, hide offering, catalog filtering

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:new_window: target="_blank"}

# Filtering the {{site.data.keyword.cloud_notm}} catalog for all account users
{: #filter-account}

This tutorial walks you through the steps to set a filter to include all {{site.data.keyword.cloud}} offerings, except for {{site.data.keyword.appid_full}}, in the {{site.data.keyword.cloud_notm}} catalog.
{: shortdesc}

This feature is available only in a closed beta program. If you’re interested in participating, contact kala.nenkova@ibm.com.
{: note}

## Before you begin
{: #prereqs-acctfilter}

To complete this tutorial, you need to be assigned the administrator role on the private catalog service. With this type of access, you can set filters in the {{site.data.keyword.cloud_notm}} catalog for all users in the account. For more information, see [Assigning users access](/docs/account?topic=account-catalog-access).

  If you don't see what you're expecting in the console based on your permissions, try refreshing your session by going to https://cloud.ibm.com/login.
  {: tip} 

## Set a catalog filter in the console
{: #create-acctfilter}

Complete the following steps to set a filter that includes all {{site.data.keyword.cloud_notm}} offerings in the catalog except for {{site.data.keyword.appid_short_notm}}.

1. Log in to your {{site.data.keyword.cloud_notm}} account, and go to [Manage > Catalogs](https://cloud.ibm.com/content-mgmt/catalogs).
1. Select **Settings**.
1. In the Rules section, click the **Edit** icon ![Edit icon](../icons/edit-tagging.svg).
1. Select **Exclude all offerings in the {{site.data.keyword.cloud_notm}} catalog** to start with an empty catalog.   
1. Click **Add another rule**, select **Provider**, and click **IBM**. 
1. Click **Add exception**, and select **Exclude** > **{{site.data.keyword.appid_short_notm}}**.
1. Expand the Filter preview section to verify that {{site.data.keyword.appid_short_notm}} is not included in the list of offerings. 
1. Click **Update** to apply your filter. 

## Set a catalog filter by using the CLI 
{: #cli-acctfilter}

Before you start this task, make sure your [install the {{site.data.keyword.cloud_notm}} CLI and the catalogs management CLI plug-in](/docs/account?topic=account-manage-catalog#landing-prereqs).
<br>

Complete the following steps to set a filter that includes all {{site.data.keyword.cloud_notm}} offerings in the catalog except for {{site.data.keyword.appid_short_notm}}.  
1. Remove the existing filter that you created in the previous steps.
    ```
    ibmcloud catalog filter delete
    ```
    {: codeblock}
    
1. Create a filter that includes only {{site.data.keyword.cloud_notm}} offerings in the catalog and excludes {{site.data.keyword.appid_short_notm}} from the catalog.
    ```
    ibmcloud catalog filter create --include-all false --provider ibm_created --exclude-list appid
    ```
    {: codeblock}

## Next steps
{: #next-acctfilter}

A user in the account validates that they can view all catalog offerings except {{site.data.keyword.appid_short_notm}}. See [Validating the account-level catalog filters](/docs/account?topic=account-validate-acctfilter) for more information.

### Providing feedback
{: #survey-acctfilters}

We put together a [survey](https://airtable.com/shrOeKPjUz5bzw02c){: external} specifically about this tutorial. We'd love to know what you think!

