---

copyright:
  years: 2022, 2024
lastupdated: "2024-02-01"

keywords: onboard software, Terraform, virtual server image, virtual machine image, image, vm, vsi, validate, test, VSI image, VM image, private catalog, vpc, virtual private cloud

subcollection: account

content-type: tutorial
services: cloud-object-storage, vpc
account-plan: paid
completion-time: 20m

---

{{site.data.keyword.attribute-definition-list}}

# Onboarding a virtual server image for VPC
{: #catalog-vsivpc-tutorial}
{: toc-content-type="tutorial"}
{: toc-services="cloud-object-storage, vpc"}
{: toc-completion-time="20m"}

This tutorial walks you through how to onboard a sample virtual server image for virtual private cloud (VPC) to your account. By completing this tutorial, you learn how to create a private catalog, import the image, validate that it can be installed on a selected deployment target, and make the virtual server image available to users who have access to your account. As you complete the tutorial, adapt each step to match your organization's goal. This tutorial includes steps for deploying a virtual server image to a target {{site.data.keyword.cloud_notm}} Virtual Private Cloud (VPC). As a result, you incur associated infrastructure charges.
{: shortdesc}

Onboarding Virtual Server Images for VPC with {{site.data.keyword.IBMz}} deployment support is available in private catalogs. The onboarding experience for {{site.data.keyword.IBMz_notm}}-supported Virtual Server Images is the same as how you onboard other Virtual Server Images in your private catalog.
{: note}

## Before you begin
{: #catalog-vsivpc-prereqs}

1. Verify that you're using a Pay-As-You-Go or Subscription account. See [Viewing your account type](/docs/account?topic=account-account_settings#view-acct-type) for more details.
1. Virtual server images for VPC must first be imported and validated in your VPC. If your virtual server image is already imported and validated in your VPC, you can skip these steps:
   1. Create your [VPC](/docs/vpc?topic=vpc-getting-started).
   1. Create an instance of [{{site.data.keyword.cloud_notm}} Object Storage](/docs/cloud-object-storage?topic=cloud-object-storage-getting-started-cloud-object-storage) and upload your image to a bucket.
   1. [Import and validate](/docs/vpc?topic=vpc-importing-custom-images-vpc&interface=ui) your custom image in your VPC. Do this for each region in which you want your software to be available and verify that the SHA or checksum matches for the imported image in each region.
1. Make sure you're assigned the {{site.data.keyword.cloud_notm}} Identity and Access Management (IAM) editor role or higher on the catalog management service. See [Assigning access to account management services](/docs/account?topic=account-account-services) for more information.

## Create a private catalog
{: #catalog-vsivpc-create}
{: step}

1. In the {{site.data.keyword.cloud_notm}} console, go to **Manage** > **Catalogs**, and click **Create a catalog**.
1. Select **Product default** as the catalog type.
1. Enter the name of your catalog, for example, `Sample virtual server image`.
1. Select **No products** to exclude all products in the {{site.data.keyword.cloud}} catalog from your catalog.
1. Click **Create**.

## Import the virtual server image to your private catalog
{: #catalog-vsivpc-import}
{: step}

1. From the Private products page, click **Add**.
1. Select **Virtual server image for VPC** as the deployment method.
1. Select **Software** as the kind of product that you're adding.
1. Select the image you'd like to onboard.

   If the virtual server image you want to add is not included in the list of available images, click **Import a new image** to import it. Your image must be imported into IBM Cloud VPC, in an available status, with an x86 or s390x architecture in order for you to onboard it to a private catalog. Also, your image can't be used with a bare metal profile or instance groups, or encrypted. An image can only be added to one product within one private catalog at a time. If the image you want to import is already imported into another product, you must remove the image from that product or delete the product before you add the image to a new product.
   {: tip}

1. Enter the software version, for example, `1.0.0`.
1. Select **Developer tools** as the category.
1. Click **Add product**.

## Review the image details
{: #catalog-vsivpc-review-images}
{: step}

1. From the Version list table, click the row that contains your virtual server image.
1. Review your images and click **Add region** if you want to add an image from another region. Images that you add must have the same digest or checksum as the original image that you added in step 2.
1. After you review your images, click **Next**.

## Review the version details
{: #catalog-vsivpc-review-version}
{: step}

Review the details of this version of your software, and click **Next**.

## Set the license requirements
{: #catalog-vsivpc-cfg-license}
{: step}

If users are required to accept any license agreements beyond the {{site.data.keyword.cloud_notm}} Services Agreement, provide the URL to each agreement. Or, if users can bring their own licenses, you can provide that URL as well.

1. Click **Add license**.
2. Enter the name and URL of the license, and click **Add license**.
3. Click **Next**.

## Edit your readme file
{: #catalog-vsivpc-onboard-readme}
{: step}

Use the [readme file template](/media/docs/downloads/software/sw-readme-tab-template.md){: external} to document the instructions for installing your software. For the purposes of this tutorial, the following steps describe how to edit the description of the readme file.

1. Click the **Edit** icon ![Edit icon](../icons/edit-tagging.svg "Edit").
1. Copy and paste the contents of the [readme file template](/media/docs/downloads/software/sw-readme-tab-template.md){: external} and make updates as needed.
1. Click **Save** > **Next**.

## Validate the virtual server image
{: #catalog-vsivpc-validate}
{: step}

Validating your virtual server image involves running a test deployment of your software. Validating your image proves that it's provisionable with your VPC. The first image you added to your product is validated. Additional regions are not included in this validation.

1. Configure the validation target by selecting a VPC, an SSH key, a subnet, and a profile. Then, cilck **Next**.
1. Optionally, configure the Schematics workspace by specifying a name and selcting a resource group and a Schematics region. Then, click **Next**.

   In the **Tags** field, you can enter a name of a specific tag to attach to your virtual server image. Tags provide a way to organize, track usage costs, and manage access to the resources in your account.
   {: tip}

1. In the Validation version section, select **I have read and agree to the following license agreements**.
1. Click **Validate**.

   To monitor the progress of the validation process, click **View logs**.
   {: tip}

{{_include-segments/manage-compliance-segment.md}}

## Review requirements
{: #catalog-vsivpc-review-reqs}
{: step}

You must complete validation and any other requirements to share your product to your account. When you're ready to share your product, click **Ready to share**. As a result, the virtual server image is available only to users who have access to the `Sample virtual server image` private catalog in your account.

## Next steps
{: #catalog-vsivpc-publish}

If you want to share your product to your account or enterprise as well as your private catalog, click the name of the product in the navigation to go to the product details page. From the **Actions** menu, click **Share**. Select where you want to share your product, and click **Share**.

You can also use the Partner Center to publish your product to the IBM Cloud catalog. If you publish your product to the IBM Cloud catalog, it will be publicly available to all IBM Cloud users. For more information, see [Publishing your software](/docs/sell?topic=sell-sw-publish).
