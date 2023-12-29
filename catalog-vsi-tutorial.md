---

copyright:
  years: 2022, 2023
lastupdated: "2023-12-29"

keywords: onboard software, Terraform, virtual server image, virtual machine image, image, vm, vsi, validate, test, VSI image, VM image, private catalog

subcollection: account

content-type: tutorial
services: cloud-object-storage, vpc
account-plan: paid
completion-time: 20m

---

{{site.data.keyword.attribute-definition-list}}

# Onboarding a virtual server image with Terraform
{: #catalog-vsi-tutorial}
{: toc-content-type="tutorial"}
{: toc-services="cloud-object-storage, vpc"}
{: toc-completion-time="20m"}

Onboarding virtual server images with Terraform is deprecated. After 29 March 2024, onboarding virtual server images with Terraform is no longer supported as a delivery method, which means that no new virtual server images with Terraform can be onboarded. Existing VSIs in the {{site.data.keyword.cloud_notm}} catalog will be available to use, but to take advantage of version updates and ensure continued support, onboard virtual server images for Virtual Private Cloud directly. For more information, see [Onboarding a virtual server image for VPC](/docs/account?topic=account-catalog-vsivpc-tutorial).
{: deprecated}

This tutorial walks you through how to onboard a sample virtual server image with Terraform to your account. By completing this tutorial, you learn how to create a private catalog, import the sample, validate that it can be installed on a selected deployment target, and make the virtual server image available to users who have access to your account.
{: shortdesc}

This tutorial uses [sample Terraform code](https://github.com/IBM-Cloud/isv-vsi-product-deploy-sample){: external} as part of the process to onboard a virtual server image. As you complete the tutorial, adapt each step to match your organization's goal.

The tutorial includes steps for deploying a virtual server image to a target {{site.data.keyword.cloud_notm}} Virtual Private Cloud (VPC). As a result, you incur associated infrastructure charges.
{: note}

## Before you begin
{: #catalog-vsi-prereqs}

1. Create an instance of [{{site.data.keyword.cloud_notm}} Object Storage](/docs/cloud-object-storage?topic=cloud-object-storage-getting-started-cloud-object-storage) and upload your image to a bucket.
2. Create your [VPC](/docs/vpc?topic=vpc-getting-started).
3. [Import your custom image to all regions](https://github.com/IBM-Cloud/isv-vsi-product-deploy-sample/tree/main#import-your-custom-image-to-all-supported-regions){: external} in which you want your software to be available.
4. Create your [Terraform template](/docs/schematics?topic=schematics-create-tf-config).
5. Upload your Terraform template to your GitHub repository. Use the [latest release of the sample Terraform code](https://github.com/IBM-Cloud/isv-vsi-product-deploy-sample/releases/tag/v1.0 ){: external} as an example of how to set up your repository.
6. Make sure you're assigned the {{site.data.keyword.cloud_notm}} Identity and Access Management (IAM) editor role on the catalog management service. See [Assigning access to account management services](/docs/account?topic=account-account-services) for more information.

## Create a private catalog
{: #catalog-vsi-create}
{: step}

1. In the {{site.data.keyword.cloud_notm}} console, go to **Manage** > **Catalogs**, and click **Create a catalog**.
1. Select **Product default** as the catalog type.
1. Enter the name of your catalog, for example, `Sample virtual server image`.
1. Select **No products** to exclude all products in the {{site.data.keyword.cloud}} catalog from your catalog.
1. Click **Create**.

## Import the virtual server image to your private catalog
{: #catalog-vsi-import}
{: step}

1. From the Private products page, click **Add**.
1. Select **Virtual server image with Terraform** as the deployment method.
1. Confirm that **Public repository** is selected as the repository type.
1. Enter `https://github.com/IBM-Cloud/isv-vsi-product-deploy-sample/releases/download/v1.0/isv-vsi-product-deploy-sample.tar.gz` as your source URL.
1. Enter `1.0.0` as the software version.
1. Select **Developer tools** as the category.
1. Click **Add product**.

## Review the version details
{: #catalog-vsi-review-version}
{: step}

1. From the Version list table, click the row that contains your virtual server image.
1. Review your version details from the Review the version details section. After you review your version details, click **Next**.

## Configure the deployment details
{: #catalog-vsi-cfg-deployment}
{: step}

1. If you need to specify the Terraform runtime version that you want Schematics to use, click the **Override the default Terraform runtime version** checkbox and enter a version.
1. From the Configure the deployment details section, click **Add deployment values**.
1. Select **Parameter** to select all options, and click **Add**.
1. To customize which parameters are required for users to specify during the installation and which ones are hidden altogether, select a parameter and click **Edit**. For the purposes of this tutorial, configure each parameter as described in the following table.

| Parameter | Description | Required for users to specify? | Hidden from users? |
| --- | --- | --- | --- |
| `TF_VERSION` | The version of the Terraform engine that's used in the Schematics workspace. | `False` | `True` |
| `region` | The region in which the VPC instance is located. | `True` | `False` |
| `ssh_key_name` | The name of the public SSH key to use when creating the virtual server instance. | `True` | `False` |
| `subnet_id` | The ID of the subnet within the VPC that the virtual server instance uses. | `True` | `False` |
| `vsi_instance_name` | The name of the virtual server instance. | `True` | `False` |
| `vsi_profile` | The profile of compute CPU and memory resources to use when creating the virtual server instance. | `False` | `False` |
| `vsi_security_group` | The name of the security group that is created. | `True` | `False` |
{: caption="Table 1. Parameters that you need to configure" caption-side="bottom"}

{{site.data.content.output-values}}

{{site.data.content.define-IAM-access}}

## Set the license requirements
{: #catalog-vsi-cfg-license}
{: step}

If users are required to accept any license agreements beyond the {{site.data.keyword.cloud_notm}} Services Agreement, provide the URL to each agreement. Or, if users can bring their own licenses, you can provide that URL as well.

1. Click **Add license agreements** > **Add**.
2. Enter the name and URL, and click **Update**.
3. Click **Next**.

## Review your readme file
{: #catalog-vsimage-onboard-readme}
{: step}

The TGZ file that you imported to your private catalog includes a readme file that provides product information for the virtual server image. If you want to make updates to the readme file, you can edit it directly from your private catalog. For the purposes of this tutorial, the following steps describe how to edit the description of the readme file.

1. Click the **Edit** icon ![Edit icon](../icons/edit-tagging.svg "Edit"), and update the description with the following sentence:

   `Create and deploy a virtual server with ease by using a custom image.`

1. Click **Save** > **Next**.

## Validate the virtual server image
{: #catalog-vsi-validate}
{: step}

1. From the Validate product tab, enter the name of your Schematics workspace, select a resource group, select a Schematics region, and click **Next**.

   In the **Tags** field, you can enter a name of a specific tag to attach to your virtual server image. Tags provide a way to organize, track usage costs, and manage access to the resources in your account.
   {: tip}

1. From the Deployment values section, review your parameter values, and click **Next**.
1. In the Validation product section, select **I have read and agree to the following license agreements**.
1. Click **Validate**.

   To monitor the progress of the validation process, click **View logs**.
   {: tip}

## Manage compliance
{: #catalog-vsi-controls}
{: step}

Controls are safeguards that are used to meet security and compliance requirements. Only controls that are supported by Security and Compliance Center, formatted correctly, and validated by Code Risk Analysis and Security and Compliance Center scans appear in the catalog. For more information, see [Adding compliance details](/docs/account?topic=account-catalog-format-controls).

### Manage compliance controls
{: #catalog-vsi-add-controls}

You can review the controls that were added from your readme file and add additional controls.

1. Click **Add controls**.
1. Choose a profile.
1. Select the controls that you want to add to your version.
1. Click **Add**.

### Run Code Risk Analyzer scan
{: #catalog-vsi-cra-scan}

Scan your source code with Code Risk Analyzer to identify any security vulnerabilities that you need to assess.

1. Click **Run scan**.
2. Wait for the scan to finish.

### Add Security and Compliance Center scan
{: #catalog-vsi-scc-scan}

Add the scans that you previously ran in the Security and Compliance Center. Security and Compliance Center scans determine adherence to regulatory controls. For more information, see [Scheduling a scan](/docs/security-compliance?topic=security-compliance-scan-resources&interface=ui#scan-schedule-ui).

1. Select the profile that you scanned.
1. Select the Security and Compliance Center scan.
1. Click **Add scan**.
1. Click **Next**.

## Review requirements
{: #catalog-vsi-review-reqs}

You must complete validation and any other requirements to publish your product to your account.

## Next steps
{: #catalog-vsi-publish}

After you onboard and validate your virtual server image, you're ready to publish it to your account. From the **Actions** menu, select **Publish to account**. As a result, the virtual server image is available only to users who have access to the `Sample virtual server image` private catalog in your account.
