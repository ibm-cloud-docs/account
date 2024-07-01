---

copyright:
  years: 2022, 2023
lastupdated: "2023-02-08"

subcollection: account

keywords: objects, private catalog, onboarding, preset configuration, preset, JSON object, JSON, preset configuration catalog, preset configuration private catalog

---

{{site.data.keyword.attribute-definition-list}}


# Creating preset configurations for your private catalog
{: #preset-config-onboard-catalog}

When users deploy software, configuring input variables is often required. These input variables can be configured in the {{site.data.keyword.cloud_notm}} UI at the time of deployment, but this process can be tedious and prone to human error. Instead, you can create a preset configuration that contains all of the input variable configurations for a specific Terraform-based software. When users deploy that software, they can select a preset configuration instead of configuring each input variable manually.
{: shortdesc}

Using preset configurations can speed up the deployment process for a specific software. Let's say you're a consultant, and you travel to different client sites to set up environments with many complicated input variables to configure. Create a preset configuration so all of the input variables can be configured with a single click when you deploy.

Preset configurations provide more control over the deployment of a specific software. Instead of configuring each input variable manually, users can deploy software with a preset configuration selected. Doing so ensures that the software is deployed with the correct input variables configured.

## What's in a preset configuration?
{: #preset-config-whats-in}

Preset configurations are created as JSON objects in the {{site.data.keyword.cloud_notm}} console. When you create your preset configuration, you'll need to include the following information in your object's data:
* A URL to an icon that represents your preset configuration.
* A long description of your preset configuration.
* Information about the offering that your preset configuration is targeting, such as the ID of the target offering and the ID of the catalog that contains the target offering.
* The key value pairs that define the input variables that are applied when the user deploys the target offering with the preset configuration selected. Make sure that your input variable names and structure matches up with the names and structure of the input variables in the target offering.
* An architecture diagram for your preset configuration.

If you want your preset configuration to be publicly available, select a parent product. You must have editor access to the parent product, and it must be published to the {{site.data.keyword.cloud_notm}} catalog. If you don’t select a parent, you can still share your preset configuration to your account or enterprise, but you won't be able to publish it publicly.

## Before you begin
{: #onboard-preset-prereq}

1. Make sure you're assigned the [administrator role on the catalog management service](/docs/account?topic=account-account-services#catalog-management-account-management) to complete this task.
1. Verify that you're using a Pay-As-You-Go or Subscription account. See [Viewing your account type](/docs/account?topic=account-account_settings#view-acct-type) for more details.

## Creating a private catalog for your preset configurations
{: #create-preset-catalog}
{: ui}

Like products, preset configurations in {{site.data.keyword.cloud_notm}} are organized into catalogs. To create a preset configuration, you must first create a preset configuration catalog to contain it.

All private catalogs that are in an account inherit filters that are set by the account owner or administrator at the account level. In addition, if the account is a parent account in an {{site.data.keyword.cloud_notm}} enterprise, the filters apply to all child account groups and accounts.
{: note}

Complete the following steps to create a private catalog for your preset configurations:

1. Go to **Manage** > **Catalogs**, in the {{site.data.keyword.cloud_notm}} console, and click **Create a catalog**.
1. Select the **Preset configuration** catalog type.
1. Enter a name and description.
1. Click **Create**.

To authorize users to work with the preset configurations in your private catalogs, assign them the [viewer role on the catalog management service](/docs/account?topic=account-account-services#catalog-management-account-management).
{: tip}

## Creating your preset configuration
{: #create-preset}
{: ui}

Complete the following steps to to create a preset configuration in your private catalog:

1. In the {{site.data.keyword.cloud_notm}} console, go to **Manage** > **Catalogs**, select **Private catalogs**.
1. Select the private catalog where you want to add your preset configuration.
   You can only add preset configurations to preset configuration catalogs. You can't add preset configurations to a product catalog or a Virtual Private Endpoint (VPE) catalog.
   {: note}

1. To add a preset configuration to your private catalog, click **Add**.
1. Enter a display name and optionally select a parent product. Selecting a parent product connects the preset configuration to a published product in the IBM Cloud catalog. You must select a parent product if you want to publish your preset configuration publicly.
1. Click **Add**.
1. Click **Edit** to modify the JSON object with your preset configuration's unique values.
1. Click **Save**.

## Creating your preset configuration by using the CLI
{: #create-preset-cli}
{: cli}

To create and add a preset configuration to your private catalog, use the following steps:

1. Create a new filter.
   ```bash
   ibmcloud catalog object create vpe [--catalog CATALOG] [--crn CRN] [--endpoint-type TYPE] [--fqdn FQDN] [--name NAME] [--region REGION]
   ```
   {: codeblock}

   If you have multiple values for the `fqdn` flag, you can list the values separated by a comma. For example, `--fdqn "example.com, example2.com"`.

For more information about this command, enter:
```bash
ibmcloud catalog object help create vpe
```
{: codeblock}

<!--
## Next steps
{: #next-steps-preset}

After you added a preset configuration to your private catalog, you need to [validate your object's data format](/docs/get-coding?topic=get-coding-vpe-onboarding-platform#validate-vpe-object). --!>
