---

copyright:
  years: 2022, [{CURRENT_YEAR}]
lastupdated: "2024-02-01"

keywords: onboard software, Terraform, virtual server image, virtual machine image, image, vm, vsi, validate, test, VSI image, VM image, private catalog, power, power systems, power systems virtual server

subcollection: account

content-type: tutorial
services: cloud-object-storage, vpc
account-plan: paid
completion-time: 20m

---

{{site.data.keyword.attribute-definition-list}}

# Onboarding a virtual server image for {{site.data.keyword.powerSys_notm}}
{: #catalog-vsipower-tutorial}
{: toc-content-type="tutorial"}
{: toc-services="cloud-object-storage, vpc"}
{: toc-completion-time="20m"}

This tutorial walks you through how to onboard a sample virtual server image for {{site.data.keyword.powerSys_notm}} to your account. By completing this tutorial, you learn how to create a private catalog, import the sample, validate that it can be installed on a selected deployment target, and make the virtual server image available to users who have access to your account.
{: shortdesc}

This tutorial uses a [sample virtual server image for Power Systems Virtual Server](https://github.com/IBM-Cloud/isv-power-vsi-product-deploy-sample){: external} as part of the process to onboard a virtual server image. As you complete the tutorial, adapt each step to match your organization's goal.

The tutorial includes steps for deploying a virtual server image to a target {{site.data.keyword.powerSys_notm}}. As a result, you incur associated infrastructure charges.
{: note}

## Before you begin
{: #catalog-vsipower-prereqs}

1. Verify that you're using a Pay-As-You-Go or Subscription account. See [Viewing your account type](/docs/account?topic=account-account_settings#view-acct-type) for more details.
1. Create your {{site.data.keyword.powerSys_notm}} instance [and convert it into a public image](/docs/power-iaas?topic=power-iaas-virtual-appliances#onboard-vsi).
1. After your image is converted into a public image, create your [Terraform template](/docs/schematics?topic=schematics-create-tf-config).
1. [Upload your Terraform template and readme file to your GitHub repository](https://github.com/IBM-Cloud/isv-vsi-product-deploy-sample/tree/main#upload-your-terraform-template-to-a-github-release){: external}.

   Use the [latest release of the sample code](https://github.com/IBM-Cloud/isv-power-vsi-product-deploy-sample ){: external} as an example of how to set up your repository.
   {: tip}

1. Make sure you're assigned the {{site.data.keyword.cloud_notm}} Identity and Access Management (IAM) editor role on the catalog management service. See [Assigning access to account management services](/docs/account?topic=account-account-services) for more information.

## Create a private catalog
{: #catalog-vsipower-create}
{: step}

1. In the {{site.data.keyword.cloud_notm}} console, go to **Manage** > **Catalogs**, and click **Create a catalog**.
1. Select **Product default** as the catalog type.
1. Enter the name of your catalog, for example, `Sample virtual server image`.
1. Select **No products** to exclude all products in the {{site.data.keyword.cloud}} catalog from your catalog.
1. Click **Create**.

## Import the virtual server image to your private catalog
{: #catalog-vsipower-import}
{: step}

1. From the Private products page, click **Add**.
1. Select **Virtual server image for Power Systems** as the deployment method.
1. Confirm that **Public repository** is selected as the repository type.
1. Enter `https://github.com/IBM-Cloud/isv-power-vsi-product-deploy-sample` as your source URL.
1. Enter `1.0.0` as the software version.
1. Click **Add product**.

## Review the version details
{: #catalog-vsipower-review-version}
{: step}

1. From the Version list table, click the row that contains your virtual server image.
1. Review your version details from the Review the version details section. After you review your version details, click **Next**.

## Configure the deployment details
{: #catalog-vsipower-cfg-deployment}
{: step}

1. If you need to specify the Terraform runtime version that you want Schematics to use, click the **Override the default Terraform runtime version** checkbox and enter a version.
1. From the Configure the deployment details section, click **Add deployment values**.
1. Select **Parameter** to select all options, and click **Add**.
1. To customize which parameters are required for users to specify during the installation and which ones are hidden altogether, select a parameter and click **Edit**. For the purposes of this tutorial, configure each parameter as described in the following table.

| Parameter | Description | Required for users to specify? | Hidden from users? |
| --- | ---------- | --- | --- |
| **`crn`** | The {{site.data.keyword.powerSys_notm}} CRN | `True` | `False` |
| **`instance_name`** | The name of the virtual server instance. | `True` | `False` |
| **`memory`** | The amount of memory that you want to assign to your instance in gigabytes. | `False` | `False` |
| **`network_name`** | The network ID or name to assign to the instance, as defined for the selected {{site.data.keyword.powerSys_notm}} CRN. | `True` | `False` |
| **`processor_type`** | The type of processor mode in which the VM runs. Specify `shared`, `capped`, or `dedicated`. | `False` | `False` |
| **`processors`** | The number of vCPUs to assign to the VM as visible within the guest OS. | `False` | `False` |
| **`ssh_key_name`** | The name of the public SSH RSA key to use when you create the instance, as defined for the selected {{site.data.keyword.powerSys_notm}} CRN. | `True` | `False` |
| **`sys_type`** | The type of system on which to create the VM: `s922`, `e880`, `e980`, `e1080`, or `s1022`. | `False` | `False` |
{: caption="Deployment values for a virtual server image" caption-side="top"}

Next, update the configuration type of the **`crn`** and **`processors`** parameters:

1. From the Deployment values table, select the **`crn`** parameter and click **Edit**.
1. Open the **Value details** menu and select **Power Systems Virtual Server**.
1. Click **Save**.
1. From the Deployment values table, select the **`processors`** parameter and click **Edit**.
1. Open the **Value details** menu and select **Float**.

{{_include-segments/edit-output-segment.md}}

{{_include-segments/define-iam-segment.md}}

## Set the license requirements
{: #catalog-vsipower-cfg-license}
{: step}

If users are required to accept any license agreements beyond the {{site.data.keyword.cloud_notm}} Services Agreement, provide the URL to each agreement. Or, if users can bring their own licenses, you can provide that URL as well.

1. Click **Add license agreements** > **Add**.
2. Enter the name and URL, and click **Update**.
3. Click **Next**.

## Review your readme file
{: #catalog-vsipower-onboard-readme}
{: step}

The TGZ file that you imported to your private catalog includes a readme file that provides product information for the virtual server image. If you want to make updates to the readme file, you can edit it directly from your private catalog. For the purposes of this tutorial, the following steps describe how to edit the description of the readme file.

1. Click the **Edit** icon ![Edit icon](../icons/edit-tagging.svg "Edit"), and update the description with the following sentence:

`Create and deploy a virtual server with ease by using a custom image.`

1. Click **Save** > **Next**.

## Validate the virtual server image
{: #catalog-vsipower-validate}
{: step}

Validate that you can deploy the virtual server image to your {{site.data.keyword.powerSys_notm}} instance.

1. From the Validate product tab, enter the name of your Schematics workspace, select a resource group, select a Schematics region, and click **Next**.

   In the **Tags** field, you can enter a name of a specific tag to attach to your virtual server image. Tags provide a way to organize, track usage costs, and manage access to the resources in your account.
   {: tip}

1. From the Deployment values section, review your parameter values, and click **Next**.
1. In the Validation product section, select **I have read and agree to the following license agreements**.
1. Click **Validate**.

   To monitor the progress of the validation process, click **View logs**.
   {: tip}

{{_include-segments/manage-compliance-segment.md}}

## Review requirements
{: #catalog-vsipower-review-reqs}

You must complete validation and any other requirements to publish your product to your account.

## Next steps
{: #catalog-vsipower-publish}

After you onboard and validate your virtual server image, you're ready to publish it to your account. From the **Actions** menu, select **Publish to account**. As a result, the virtual server image for Power Systems is available only to users who have access to the `Sample virtual server image` private catalog in your account.
