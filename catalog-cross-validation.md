---

copyright:
  years: 2023
lastupdated: "2023-07-05"

keywords: catalog, private catalogs, IAM access, Schematics service, cross accounts, target account

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Setting up a target account
{: #catalog-cross-validation}

If you want to use a different account to validate your product and run security and compliance scans, you can add a target account. You can add a target account by using an IBM Cloud API key or a trusted profile ID.
{: shortdesc}

You might want to use a target account for the following reasons:

- Prevent the account with the product from becoming cluttered with resources that are created and deleted as part of the onboarding process
- Allow users to complete onboarding when they might not have authorization to create resources in the account that contains the product

## Before you begin
{: #catalog-cross-begin}

1. Verify that you're using a Pay-As-You-Go or Subscription account. See [Viewing your account type](/docs/account?topic=account-account_settings#view-acct-type) for more details.
1. Make sure you have the [administrator role on the catalog management service](/docs/account?topic=account-account-services#catalog-management-account-management) or have the catalog administrator complete this task.
1. Set up [service-to-service authorization](/docs/account?topic=account-catalog-catalog-service-authorization).
1. If you want to use an IBM Cloud API key, [create an API key](/docs/account?topic=account-userapikey&interface=ui#create_user_key) for the target account.
1. If you want to use a trusted profile ID, see [Creating trusted profiles](/docs/account?topic=account-create-trusted-profile&interface=ui).

<!--
1. Install or update to the latest version of the [{{site.data.keyword.cloud_notm}} CLI](/docs/cli?topic=cli-install-ibmcloud-cli).{: cli}
1. Install the [Catalog Management CLI plug-in](/docs/cli?topic=cli-manage-catalogs-plugin#install-managecatalogs).{: clil}
1. [Import a version of your product to a private catalog](/docs/account?topic=account-create-private-catalog&interface=ui) but stop before the validation step.{: cli}
-->

## Using an IBM Cloud API key
{: #target-api-key}

You can add a target account by using an API key. Alternatively, if you would like to add a trusted profile ID, see [Using a trusted profile](/docs/account?topic=account-catalog-cross-validatione&interface=ui#target-trusted-profile).

1. In the {{site.data.keyword.cloud_notm}} console, click the **Menu** icon ![Menu icon](../icons/icon_hamburger.svg) > **Manage** > **Catalogs** > **Private catalogs** to access your private catalogs.
1. Select the private catalog that you want add a target account to.
1. Click **Actions...** > **Edit catalog details** > **Add** to add a target account.
1. Select **IBM Cloud API key** as the method.
1. Create a programmatic name of the target account.
1. Create a display name for the target account. The display name appears as a target account option for users that are onboarding products.
1. Enter the API key for the target account. If you need an API key, see [Create an API key](/docs/account?topic=account-userapikey&interface=ui#create_user_key).
1. Click the checkbox to indicate that you set you service authorization for Schematics and Catalog management.
1. Click **Add** > **Update**.

Users can now use the added target account to validate and add scans to any product version in the private catalog.

## Using a trusted profile
{: #target-trusted-profile}

If you want to use a trusted profile, you need to update your trusted profile to include the private catalog's CRN as a trust relationship. If you need to create a trusted profile, see [Creating trusted profiles](/docs/account?topic=account-create-trusted-profile&interface=ui).

### Updating a trusted profile
{: #update-create-profile}

1. In the {{site.data.keyword.cloud_notm}} console, click the **Menu** icon ![Menu icon](../icons/icon_hamburger.svg) > **Manage** > **Catalogs** > **Private catalogs** to access your private catalogs.
1. Select the private catalog that you want add a target account to.
1. Click **Actions...** > **Edit catalog details** to find the `Catalog CRN`.
1. Copy the `Catalog CRN`.
1. Click the **Menu** icon ![Menu icon](../icons/icon_hamburger.svg) > **Manage** > **Access (IAM)** > **Trusted profiles** to access your existing trusted profile.
1. Select the trusted profile that you want to use.
1. Click **IBM Cloud services** > **Add**.
1. Enter the CRN and click **Save**.
1. Click **Details** to find the `Profile ID` of the trusted profile.
1. Copy the `Profile ID`. You use the ID to add a target account to your private catalog.

You linked the private catalog to the trusted profile as a trust relationship and are ready to add a target account.

### Adding a target account
{: #target-account-trusted}

1. Click the **Menu** icon ![Menu icon](../icons/icon_hamburger.svg) > **Manage** > **Catalogs** > **Private catalogs** to access your private catalogs.
1. Select the private catalog that you want add a target account to.
1. Click **Actions...** > **Edit catalog details** > **Add** to add a target account.
1. Select **Trusted profile ID** as the method.
1. Create a unique programmatic name for the target account.
1. Create a display name for the target account. The display name appears as a target account option for users that are onboarding products.
1. Enter the profile ID of the trusted profile. If you do not have the profile ID, see [Updating a trusted profile](/docs/account?topic=account-catalog-cross-validatione&interface=ui#update-create-profile).
1. Click the checkbox to indicate that you set you service authorization for Schematics and Catalog management.
1. Click the checkbox to indicate that you created a trusted profile and added the catalog CRN as a trust relationship.
1. Click **Add** > **Update**.

Users can now use the added target account to validate and add scans to any product version in the private catalog.

<!--
## Finding the version locator for your version
{: #cross-vl-cli}
{: cli}

To successfully use a target account for validation, you must find the version locator for your version.

Run the [`ibmcloud catalog offering get`](/docs/cli?topic=cli-manage-catalogs-plugin#get-offering) to retrieve the version locator.

```bash
ibmcloud catalog offering get --catalog CATALOG --offering OFFERING_NAME [--output FORMAT]
```
{: codeblock}

## Finding the resource group
{: #cross-val-resource}
{: cli}

Before you can validate your product, you need to locate the ID of the resource group that Schematics will use to validate your product. To find the resource group, you must use the console.

1. Log in to the target {{site.data.keyword.cloud_notm}} account that contains the Schematics workspace.
1. Go to **Manage** > **Account** > **Resource groups**.
1. From the list of resource groups, copy the ID that you want to use.

## Validating your product by using a different account
{: #catalog-cross-val-steps-ui}
{: #ui}

Is there a way to do this in the UI?

## Create a file with defined deployment variables
{: #cross-var-file}

Create a JSON or TXT file that defines deployment variables and the values to use for validation.

## Validating your product by the CLI
{: #catalog-cross-val-steps-cli}
{: cli}

Using the version locator, api key, deployment file, and resource group that you retreived, you can validate the version by running the [`ibmcloud catalog offering version`](/docs/cli?topic=cli-manage-catalogs-plugin#validate-offering) command.

```bash
ibmcloud catalog offering version validate --vl <version locator> --override-values <file name> --target-api-key <api key> --workspace-rg-id <resource group id>
```
{: codeblock}


## Applying Security and Compliance Center scans by using the UI
{: #cross-scan}

Now that you have validated your version you can run Security and Compliance Center scans to prove that your version meets the requirements of the controls that you have claimed. If you have not claimed and controls, you do not need to apply any scans.

### Running a Security and Compliance Center scan
{: #cross-scan-run}

1. In the {{site.data.keyword.cloud_notm}} console, click the **Menu** icon ![Menu icon](../icons/icon_hamburger.svg) **> Security and Compliance** to access {{site.data.keyword.compliance_short}}.
1. In the navigation, click **Profile**.
1. Click the **Overflow** menu in the row of the profile that you want to evaluate and select **Run scan**.
1. Click **Run scan**.
1. After your scan completes, copy the scan ID.

### Applying a Secuirty and Compliance Center scan
{: #cross-scan-apply-ui}
{: ui}

After your scan completes and you have copied the scan ID, return to your private catalog.

### Applying a Security and Compliance Center scan
{: #cross-scan-apply-cli}
{: cli}

After your scan completes and you have copied the scan ID, you can use the [`ibmcloud catalog offering version scc-apply`](/docs/cli?topic=cli-manage-catalogs-plugin#version-scc) command to apply the scans to your product.

You need the following information to complete the scan:
 - version locator of the product version
 - scan ID of the Security and Compliance Center scans
 - the api key for the account that you used to run the scans

```bash
ibmcloud catalog offering version scc-apply --vl <version locator> --scan <scan id> --target-api-key <api key>
```

You can now return to the [onboarding steps](/docs/account?topic=account-create-private-catalog&interface=ui#catalog-manage-review-reqs) to finish onboarding your version to a private catalog.

>
