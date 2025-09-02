---

copyright:

  years: 2021, 2025
lastupdated: "2025-09-02"

keywords: private catalog, software, onboard, Terraform, terraform template

subcollection: account

content-type: tutorial
services: Terraform
account-plan: paid
completion-time: 20m

---

{{site.data.keyword.attribute-definition-list}}

# Onboarding a Terraform template
{: #catalog-terraform-template-tutorial}
{: toc-content-type="tutorial"}
{: toc-services="Terraform"}
{: toc-completion-time="20m"}

This tutorial walks you through how to onboard a Terraform template to your account. By completing this tutorial, you learn how to create a private catalog and import the template. After that, you can validate that the template can create resources, or run a script, and you can make it available to users who have access to your account.
{: shortdesc}

## Before you begin
{: #terraform-prereqs}

1. Verify that you're using a Pay-As-You-Go or Subscription account. See [Viewing your account type](https://cloud.ibm.com/docs/account?topic=account-account_settings#view-acct-type) for more details.
1. Verify that you're assigned the following roles. For more information, see [Assigning access to account management services](https://cloud.ibm.com/docs/account?topic=account-account-services) and [Managing access to resources](https://cloud.ibm.com/docs/account?topic=account-assign-access-resources).

   * Administrator on all account management services and all IAM-enabled services
   * Editor on the catalog management service
   * Manager service access role for IBM Cloud Schematics
   * Operator platform role for VPC Infrastructure
   * Editor on the software instance service
   * Required permission to complete a specific task

1. Create your [Terraform template](/docs/schematics?topic=schematics-create-tf-config).
1. To test your Terraform template, run the following commands from the Terraform CLI:

   * `terraform init`
   * `terraform validate`

1. Upload your Terraform template to a GitHub release and create a `.tgz` file. For more information, see [Upload your Terraform template and readme file to your GitHub repository](https://github.com/IBM-Cloud/isv-vsi-product-deploy-sample/tree/main#upload-your-terraform-template-to-a-github-release){: external}.

   Use this release of the [sample Terraform code](https://github.com/IBM-Cloud/isv-vsi-product-deploy-sample/releases/tag/v1.0 ){: external} as an example of how to set up your repository.
   {: tip}

## Create a private catalog
{: #catalog-terraform-private}
{: step}

Private catalogs provide a way for you to make your own products available to users in your account.

1. Go to **Manage** > **Catalogs** in the {{site.data.keyword.cloud_notm}} console, and click **Create a catalog**.
1. Select **Product default** as the catalog type.
1. Enter the name of your catalog, for example, `Sample Terraform`.
1. Select **No products** to exclude all products in the {{site.data.keyword.cloud}} catalog from your catalog.
1. Click **Create**.

## Import your Terraform template
{: #catalog-terraform-import}
{: step}

1. On the Private products page, click **Add**.
1. Select **Terraform** as your deployment method.
1. Select the type of repository.
1. Enter the **example Terraform URL** as your source URL.
1. Enter the software version in the format of major version, minor version, and revision, for example, `1.0.0`.
1. Click **Add product**.

## Review the version details
{: #catalog-terraform-review-version}
{: step}

From the Configure version tab, you can review your version details. After you review your version details, click **Next**.

## Configure the deployment values
{: #catalog-terraform-cfgdeploy}
{: step}

After you review the version details, you're ready to configure the deployment values.

1. If you need to specify the Terraform runtime version that you want Schematics to use, click the **Override the default Terraform runtime version** checkbox and enter a version.
1. From the Configure the deployment details section, click **Add deployment values**.
1. Select the **Parameter** checkbox to select all options, and click **Add**.
1. To customize which parameters are required for users to specify during the installation and which ones are hidden from users, select a parameter and click **Edit**. Click the checkboxes to configure the values and click **Save**.

{{_include-segments/edit-output-segment.md}}

{{_include-segments/define-iam-segment.md}}

## Set the license requirements
{: #catalog-terraform-license}
{: step}

If users are required to accept any license agreements beyond the {{site.data.keyword.cloud_notm}} Services Agreement, provide the URL to each agreement. Or, if users can bring their own licenses, you can provide that URL as well.

1. Click **Add license agreements** > **Add**.
2. Enter the name and URL, and click **Update**.
3. After you enter the additional license agreements, click **Next**.

## Validate the Terraform template
{: #catalog-terraform-validate}
{: step}

1. From the Validate product tab, enter the name of your workspace, select a resource group, select a Schematics region, and click **Next**.

   In the **Tags** field, you can enter a name of a specific tag to attach to your template. This tag is put on the {{site.data.keyword.bplong_notm}} workspace. Tags provide a way to organize, track usage costs, and manage access to the resources in your account.
   {: tip}

1. From the Deployment values section, review your parameter values, and click **Next**.
1. In the Validation product section, select **I have read and agree to the following license agreements**.
1. Click **Validate**.

   To monitor the progress of the validation process, click **View logs**.
   {: tip}

## Manage compliance
{: #manage-compliance}
{: step}

{{_include-segments/manage-compliance-segment.md}}

### Run a Security and Compliance Center scan
{: #run-scc-scans}

{{_include-segments/run-security-segment.md}}

### Adding compliance controls
{: #add-controls}

{{_include-segments/add-compliance-control-segment.md}}

### Applying {{site.data.keyword.compliance_short}} scans
{: #add-scc-scans}

{{_include-segments/apply-scans-segment.md}}

## Review requirements
{: #catalog-terraform-review-reqs}

You must complete validation and any other requirements to publish to your account.

## Next steps
{: #catalog-terraform-next}

After you onboard and validate your Terraform template, you're ready to publish it to your account. From the **Actions** menu, select **Publish to account**. As a result, the Terraform template is available to only users that have access to the `Sample Terraform` private catalog in your account.
