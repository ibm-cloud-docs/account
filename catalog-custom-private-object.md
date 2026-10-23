---

copyright:

  years: 2020, 2026
lastupdated: "2026-10-23"

keywords: catalog, restrict visibility, hide object, restrict by user, filter catalog, private catalog, catalog management service, public catalog

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:external: target="_blank" .external}

# Customizing objects in your private catalogs
{: #restrict-by-user-object}

Customize objects in {{site.data.keyword.cloud_notm}} private catalogs to control which virtual private endpoints your account users can access and use approved resources.
{: shortdesc}

Let's say you're an operations admin for your team, and you want your team to use only approved networks. You can create one catalog that includes all of the private virtual private endpoints for use by users in your account. Team members with viewer access can access only the virtual private endpoints in that catalog.

All private catalogs that are in an account inherit filters that are set by the account owner or administrator at the account level. In addition, if the account is a parent account in an {{site.data.keyword.cloud_notm}} enterprise, the filters apply to all child account groups and accounts.
{: tip}

## Before you begin
{: #prereq-restrict-object}

You need the [administrator role on the catalog management service](/docs/iam?topic=iam-account-services&interface=ui#catalog-management-account-management) to complete this task.

## Creating a private catalog for your objects
{: #catalog-all-object}

Complete the following steps to create a catalog for your objects:

1. Go to **Manage** > **Catalogs**, in the {{site.data.keyword.cloud_notm}} console, and click **Create a catalog**.
1. Select the **Virtual Private Endpoint** catalog type.
1. Enter a name and description.
1. Click **Create**.


## Authorizing access to private catalogs
{: #customcatalog-access-object}

To authorize users to work with the objects in your private catalogs, assign them the [viewer role on the catalog management service](/docs/iam?topic=iam-account-services&interface=ui#catalog-management-account-management).  
