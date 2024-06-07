---

copyright:
  years: 2022, 2023
lastupdated: "2023-02-07"

keywords: catalog, restrict visibility, hide object, restrict by user, filter catalog, private catalog, catalog management service, public catalog, preset configuration, preset

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Customizing preset configurations in your private catalogs
{: #restrict-by-user-preset}

Like products, preset configurations in {{site.data.keyword.cloud_notm}} are organized into catalogs. To create a preset configuration, you must first create a preset configuration catalog to contain it.
{: shortdesc}

For more information on preset configurations and the benefits to using them, go to [Creating preset configurations for your private catalog](/docs/account?topic=account-preset-config-onboard-catalog&interface=ui).

All private catalogs that are in an account inherit filters that are set by the account owner or administrator at the account level. In addition, if the account is a parent account in an {{site.data.keyword.cloud_notm}} enterprise, the filters apply to all child account groups and accounts.
{: tip}

## Before you begin
{: #prereq-restrict-preset}

You need the [administrator role on the catalog management service](/docs/account?topic=account-account-services#catalog-management-account-management) to complete this task.

## Creating a private catalog for your preset configurations
{: #catalog-all-preset}

Complete the following steps to create a catalog for your preset configurations:

1. Go to **Manage** > **Catalogs**, in the {{site.data.keyword.cloud_notm}} console, and click **Create a catalog**.
1. Select the **Preset configuration** catalog type.
1. Enter a name and description.
1. Click **Create**.

## Authorizing access to private catalogs
{: #customcatalog-access-object}

To authorize users to work with the preset configurations in your private catalogs, assign them the [viewer role on the catalog management service](/docs/account?topic=account-account-services#catalog-management-account-management).
