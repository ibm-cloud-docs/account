---

copyright:

  years: 2024, 2025
lastupdated: "2025-01-28"

keywords: onboard software, virtual server image, virtual machine image, image, vm, vsi, validate, test, VSI image, VM image, private catalog, vpc, virtual private cloud, software plan, plan, usage-based plan, partner center

subcollection: account

content-type: tutorial
services: cloud-object-storage, vpc
account-plan: paid
completion-time: 20m

---

{{site.data.keyword.attribute-definition-list}}

# Onboarding a virtual server image for VPC with a plan
{: #working-catalog-vsivpc-tutorial}
{: toc-content-type="tutorial"}
{: toc-services="cloud-object-storage, vpc"}
{: toc-completion-time="20m"}

This tutorial walks you through how to onboard a sample virtual server image for virtual private cloud (VPC) to your account with a software plan. By completing this tutorial, you learn how to create a private catalog, import the image to Partner Center, add a pricing plan, validate that it can be installed on a selected deployment target, and make the virtual server image available to users who have access to your account. As you complete the tutorial, adapt each step to match your organization's goal. This tutorial includes steps for deploying a virtual server image to a target {{site.data.keyword.cloud_notm}} Virtual Private Cloud (VPC). As a result, you incur associated infrastructure charges.
{: shortdesc}

Onboarding Virtual Server Images for VPC with {{site.data.keyword.IBMz}} deployment support is available in private catalogs. The onboarding experience for {{site.data.keyword.IBMz_notm}}-supported Virtual Server Images is the same as how you onboard other Virtual Server Images in your private catalog.
{: note}

## Before you begin
{: #working-catalog-vsivpc-prereqs}

Before you can start onboarding a virtual server image for VPC with a plan, complete the following steps:

1. Verify that you're using a Pay-As-You-Go or Subscription account. See [Viewing your account type](/docs/account?topic=account-account_settings#view-acct-type) for more details.
1. Virtual server images for VPC must first be imported and validated in your VPC. If your virtual server image is already imported and validated in your VPC, you can skip these steps:
   1. Create your [VPC](/docs/vpc?topic=vpc-getting-started).
   1. Create an instance of [{{site.data.keyword.cloud_notm}} Object Storage](/docs/cloud-object-storage?topic=cloud-object-storage-getting-started-cloud-object-storage) and upload your image to a bucket.
   1. [Import and validate](/docs/vpc?topic=vpc-importing-custom-images-vpc&interface=ui) your custom image in your VPC. Do this for each region in which you want your software to be available and verify that the SHA or checksum matches for the imported image in each region.
1. Make sure you're assigned the {{site.data.keyword.cloud_notm}} Identity and Access Management (IAM) editor role or higher on the catalog management service and Software Instance. See [Assigning access to account management services](/docs/account?topic=account-account-services) for more information.

## Create a private catalog
{: #working-catalog-vsivpc-create}
{: step}

1. In the {{site.data.keyword.cloud_notm}} console, go to **Manage** > **Catalogs**, and click **Create a catalog**.
1. Select **Product default** as the catalog type.
1. Enter the name of your catalog, for example, `Sample virtual server image`.
1. Select **No products** to exclude all products in the {{site.data.keyword.cloud}} catalog from your catalog.
1. Click **Create**.

## Add the image to your private catalog
{: #working-catalog-vsivpc-onboard}
{: step}

1. In the Products section, click **Add product**.
1. Select **Software** as the product type.
1. Select **Virtual server image for VPC** as the delivery method.
1. Select the image that you want to onboard.

   If the virtual server image you want to add is not included in the list of available images, click **Import a new image** to import it. Your image must be imported into {{site.data.keyword.cloud_notm}} VPC, in an available status, with an x86 or s390x architecture in order for you to onboard it to a private catalog. Also, your image can't be used with a bare metal profile or instance groups, or encrypted. An image can be added to one product only within one private catalog at a time. If the image you want to import is already imported into another product, you must remove the image from that product or delete the product before you add the image to a new product.
   Only images with an x86 architecture support plans.
   {: tip}

1. Enter the software version, for example, `1.0.0`.
1. Select **Developer tools** as the product category.
1. Click **Add product**.

## Import the product to Partner Center
{: #working-import-product-pc}
{: step}

You can easily import the product that your team has created from a private catalog to Partner Center and start defining your product details. To import a product from a private catalog, complete the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, click the **Navigation Menu** icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Partner Center > My products**.
1. From the **My products** page, click **Create**.
1. Select **Import existing product**, and click **Next**.
1. Select the private catalog that contains your product and click **Select catalog**.
1. Select the product that you want to import and click **Import**.

## Submit programmatic name for review
{: #working-progname-review}
{: step}

After you import your product to Partner Center, you must get approval for your product's programmatic name to complete further onboarding tasks, such as creating pricing plans. The programmatic name is different than the product's display name. This is your product’s unique ID that is used within all {{site.data.keyword.IBM_notm}} services and tools.

Your programmatic name can't be updated after you submit it for review.
{: important}

Submit your programmatic name for review by completing the following step:

* From the Product details page, review your programmatic name, and click **Submit programmatic name > Yes**.

## Create a plan
{: #working-create-plan}
{: step}

When you onboard your product to {{site.data.keyword.cloud_notm}}, you must define a pricing model for your software in Partner Center. Currently, {{site.data.keyword.cloud_notm}} supports free, usage-based, and bring your own license (BYOL) plans. For more information, see [Defining your pricing model for software](/docs/sell?topic=sell-sw-pricing). For this tutorial, we create a usage-based plan. By adding a usage-based pricing plan, you are indicating that you offer your product as a paid integrated product, and customers need to pay to use it.

When you add a usage-based pricing plan, you provide your suggested retail pricing information. However, {{site.data.keyword.IBM_notm}} reserves the right to set the final pricing for any product that is offered to customers in the {{site.data.keyword.cloud_notm}} catalog.
{: important}

To add a usage-based pricing plan to your software, complete the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, click the **Navigation Menu** icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Partner Center** > **My products**.
1. Select the product that you're onboarding, and click **Pricing**.
1. Click **Add plan > Usage-based**.
1. Provide a name for your pricing plan. This name refers to the plan name that appears in the pricing plan list on your product's catalog page when your customers select a pricing plan.
1. Provide a programmatic name for your pricing plan.
1. Select your software type. Usage metrics available within your plan depend on the type of software that is deployed under the plan.
1. Enter your software version. You must select whether you want to validate only one version or a range of versions, or add a semantic version string to match the versions you want to validate.
1. Provide a description for your pricing plan.
1. Click **Save**.

After you add a pricing plan to your software version in Partner Center, you can manage it in your catalog as well. This means that you can change the state of your plan to publish it, add features to it, deprecate it, or update certain plan details. For more information, see [Managing software plans in catalogs](/docs/account?topic=account-sw-manage-plans).

### Submit tax and EFT forms
{: #working-submit-tax-eft-sw}

For products that you offer on {{site.data.keyword.cloud_notm}} with a paid, usage-based pricing plan, you receive disbursements based on the usage in accordance with your pricing structure. To receive disbursements, you must complete and submit the EFT form and tax documentation.

To provide tax and EFT information, complete the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, click the **Navigation Menu** icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Partner Center** > **Payments to me**.
1. Download the relevant EFT form, and complete it.

    One of three types of bank documents is required to be submitted with the form. You can submit a scanned copy of a voided check or a bank letter that is signed and stamped by the bank. If you are outside of the United States, you can alternatively provide an online bank statement. The document that you provide must include the bank name, account number, routing number (or bank key or ABA), and the account holder's name.
    {: important}

1. Download the relevant tax documentation, and complete it.
1. Submit the completed documentation and bank document by email to `apremit@us.ibm.com`. Include `cloud.onboarding@ibm.com` on the email.
1. Select **I confirm that I completed and emailed all of the required documents.**.

### Provide the ECCN
{: #working-sw-eccn}

When you define your pricing model, you must provide the Export Control Classification Number (ECCN) that applies to your product. The ECCN is required for usage-based pricing plans. If you don't have your ECCN, you can find it on the [Commerce Control List](https://www.bis.doc.gov/index.php/licensing/commerce-control-list-classification/export-control-classification-number-eccn){: external}.

You must submit your tax and EFT documents and receive approval before you can provide the ECCN if you're adding a usage-based pricing plan.
{: note}

1. In the {{site.data.keyword.cloud_notm}} console, click the **Navigation Menu** icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Partner Center** > **My products**.
1. Select your product and go to **Pricing**.
1. Click **Add ECCN** and provide the ECCN for your product.
1. Click **Add**.

If you need to update your ECCN after you add it, you must contact {{site.data.keyword.cloud_notm}} Support. To contact support, you can use the following methods:

* If you have a valid Pay-As-You-Go or Subscription account, you can click **Chat with IBM** to connect with a support engineer.
* Pay-as-you-go or subscription accounts can also contact support by phone: +1-866-403-7638.

### Provide the UNSPSC
{: #working-sw-unspsc}

You must provide your ECCN before the UNSPSC.
{: note}

In addition to ECCN, you must provide the UNSPSC that applies to your product. The UNSPSC is required for usage-based pricing plans. If you need help with selecting the UNSPSC for your service, see [How to select UNSPSC codes?](https://help.ungm.org/hc/en-us/articles/360013132940-How-to-select-UNSPSC-codes){: external}.

To provide the UNSPSC code that applies to your product, complete the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, click the **Navigation Menu** icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Partner Center** > **My products**.
1. Select your product and go to **Pricing**.
1. Click **Add UNSPSC** and select the UNSPSC code for your product.
1. Click **Add**.

### Accept the agreement terms and conditions
{: #working-sw-confirm-dra}

You must sign the agreement that outlines the terms and conditions of providing a product in the {{site.data.keyword.cloud_notm}}. Or, you can upload a custom digital provider agreement in `.pdf`, `.doc`, or `.docx` file format.

Custom digital provider agreements must be reviewed and approved by {{site.data.keyword.IBM_notm}}, which increases the time it takes for you to complete the onboarding process. The uploaded files are scanned for viruses, which might take a few minutes to complete. If a virus is detected, it is recommended to run another virus scan on your file, and then try uploading it again.
{: note}

#### Digital platform reseller agreement
{: #working-sw-dra}

If you offer usage-based pricing plans, it is required to review and submit the {{site.data.keyword.IBM_notm}} Digital Platform Reseller Agreement. This legal agreement sets the terms and conditions under which providers can onboard and sell products in {{site.data.keyword.cloud_notm}}.

Complete the following steps to review and submit the {{site.data.keyword.IBM_notm}} Digital Platform Reseller Agreement:

1. In the {{site.data.keyword.cloud_notm}} console, click the **Navigation Menu** icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Partner Center** > **My company**.
1. Click **Edit**.
1. Choose **I plan to offer free and usage-based pricing plans** from the Agreements section.
1. Click the **{{site.data.keyword.IBM_notm}} Digital Platform Reseller Agreement** link to review the agreement.
1. Select **I have read and agree to the {{site.data.keyword.IBM_notm}} Digital Platform Reseller Agreement.**, and click **Save**.

## Add metrics to a plan
{: #working-add-metrics}
{: step}

If you offer a paid integrated product and add a paid pricing plan that requires customers to pay for their usage, you must add metrics to your pricing plan to aggregate your product's usage. After you add metrics to your plan, you must request an initial metering approval, so you can submit your resource usage and start reviewing your metrics.

To add metrics to your pricing plan, complete the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, click the **Navigation Menu** icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Partner Center** > **My products**.
1. Select the product that you're onboarding, and click **Pricing**.
1. Select a usage-based plan from the table and click **Add metrics**.
1. In the Usage metrics section, click **Add metrics**.
1. Complete the required fields.
1. Click **Done**.

### Add pricing plan features
{: #working-software-add-feature}

If you completed the steps to define your pricing plan, you must add a list of features for the plan. These features uniquely identify and differentiate your pricing plan and help customers choose the most suitable plan.

To publish your plan, you must add features to it.
{: important}

To add features for your software plan, complete the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, click the **Navigation Menu** icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Partner Center** > **My products**.
1. Select the product that you're onboarding, and click **Pricing**.
1. Click **Add metrics**.
1. Click **Add feature**.
1. Provide a descriptive title and a brief description for each feature.
1. Click **Save**.

## Submit your pricing plan for review
{: #working-plan-approved}
{: step}

After you create a usage-based pricing plan and add metrics to it, you must submit your plan for review and receive approval for the pricing details. By requesting approval, the changes to your metering will be reviewed, approved, and published. When the changes are approved, they are immediately available to users of your product.

To submit your pricing plan and metering for review, complete the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, click the **Navigation Menu** icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Partner Center** > **My products**.
1. Select the product that you're onboarding, and click **Pricing**.
1. Select the pricing plan that you want to request approval for, and click **Add metrics**.
1. Click **Request approval > Yes** in the Metering approval section.

## Validate the product version in your private catalog
{: #working-validate-version}
{: step}

When you add a pricing plan to your software, you must select the product versions that you want to validate. Pricing plans that you add to a product are tied to specific versions of your software, not to the overall product. Validating your virtual server image involves running a test deployment of your software. Validating your image proves that it's provisionable with your VPC. The first image that you added to your product is validated. Additional regions are not included in this validation.

To validate a product version in your catalog, complete the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, click the **Navigation Menu** icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Partner Center** > **My products**.
1. Select the product that you're onboarding, and click **Software**.
1. From the Versions table, click the version that you want to validate. This step takes you to the private catalog that you initially created in [Step 1](#working-catalog-vsivpc-create).
1. Confirm your version details and click **Next**.
1. Add end user license agreements that users are required to accept when they install your product. Click **Next**.
1. Make the required readme file updates and click **Next**.
1. Validate your version by completing the following steps:

    1. Configure the validation target by selecting a VPC, an SSH key, a subnet, and a profile. Then, click **Next**.
    1. Optionally, configure the Schematics workspace by specifying a name and selecting a resource group and a Schematics region. Then, click **Next**.
    1. Select a pricing plan to validate with your version. You can validate against plans only that are approved to be published.

1. In the Validation version section, select **I have read and agree to the end user license agreements**.
1. Click **Validate**.

   To monitor the progress of the validation process, click **Actions... > View logs**.
   {: tip}

## Review the software instance and VSI instance
{: #working-review-instance}
{: step}

You can find the software instance and the VSI instance in the {{site.data.keyword.cloud_notm}} Resource List to review the details from the software instance details page. The details page for your software instance includes information about the installed version, CRN (cloud resource name), and pricing plan.

To review your software instance details, complete the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, click the **Navigation Menu** icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Resource list** to view your list of resources.
1. Find your VSI and software instance in the Resource list table. You can filter by your product name to find your software instance more easily.
1. Select your software instance and click **View full details** to review product details.

## Gather usage information from the running software instance
{: #working-gather-usage}
{: step}

To review how customers understand and experience your pricing plan, and validate that your metered plans are correctly configured, you must submit the resource usage for your software instance. Submitting your resource usage includes calling the Usage Metering API and providing the evidence of your testing. For more information, see [Adding metrics to your software](/docs/sell?topic=sell-software-add-metrics).

To gather usage information for your pricing plan, complete the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, click the **Navigation Menu** icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Partner Center** > **My products**.
1. Go to **Pricing**, and click **Add metrics** for the pricing plan that you want to gather usage information for.
1. Click **Test estimation and metering**.
1. Click **Go to your catalog preview** to preview your product in its draft state in the catalog and estimate a price that incorporates all the metrics that you added.
    1. Select virtual private cloud as your deployment target and select the pricing plan that you want to generate an estimate for.
    1. Select **I have read and agree to the following third party terms:**, and click **Continue**.
    1. Click **Add to estimate** and select and estimate. Then, click **Save**.
    1. Click **View estimate**. This step takes you to the cost estimator, where you can review your estimate.
    1. Take a screen capture of the usage data that is generated by the estimator.
1. Click **Add file** to upload the screen capture of the usage data that was generated by the estimator.
1. Complete the steps in [Submitting resource usage to the IBM Cloud Usage Metering API](/docs/sell?topic=sell-software-add-metrics#sw-submit-evidence) to generate usage.
    1. After you generate usage for all metrics of your plan, review that usage on the [Usage page](/billing/usage){: external} in your account, and take a screen capture of the rated usage.
1. Click **Add file** to upload the screen capture of the rated usage that you reviewed on the **Usage** page.
1. Take a screen capture of the resource usage data that you previously submitted to the {{site.data.keyword.cloud_notm}} Usage Metering API.

You can upload files in `.jpeg`, `.pdf`, or `.png` file format only.
{: note}

## Publish the plan
{: #working-publish-plan}
{: step}

After your plan details are approved in Partner Center and you added features to your plan, you can make your plan available for use and change its state to `published`. To publish your plan, complete the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, click **Manage > Catalogs > Private catalogs**.
1. Select the private catalog that contains your software.
1. Select the product in your catalog with the pricing plan that you want to publish.
1. Click **Pricing plans** and select the plan that you want to publish.
1. Click **Actions... > Publish plan > Yes**.

## Submit your product for review
{: #working-mark-version}
{: step}

Before you can publish your product, you must submit your software for approval with a version in the `ready` state. To submit a request to publish your product and make a version ready, complete the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, click the **Navigation Menu** icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Partner Center** > **My products**.
1. Select your product.
1. Review the details on each page to ensure that everything is accurate.
1. From the Onboarding checklist, click **Request approval**, and select the product version that you want to submit for publishing approval.
1. To make a specific product version ready for publishing approval, click **Make ready**.
1. Select **I confirm that my company is authorized to use all materials**.
1. Click **Request approval**.

Your request is reviewed by {{site.data.keyword.IBM_notm}} to ensure the required details, such as the product name, catalog entry, product page, pricing model, and support experience are complete and accurate. When your request is approved, you receive an email that notifies you that you can share your product.

If updates are required, you receive a separate email with details about the required updates. If you have questions about the feedback, from the My products page click the **Help** icon ![Help icon](../icons/help.svg "Help"), and then click **Contact us**. After you address all review feedback, you can submit another publishing request.
{: note}

## Publish your product
{: #working-publish-product}
{: step}

To publish your software to the {{site.data.keyword.cloud_notm}} catalog after you receive approval, complete the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, click the **Navigation Menu** icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Partner Center** > **My products**.
1. Select the product that you want to publish.
1. Click **Publish**.
1. Select **{{site.data.keyword.cloud_notm}} catalog**.
1. Click **Publish version**.

After you publish your product to the {{site.data.keyword.cloud_notm}} catalog, it will be publicly available to all {{site.data.keyword.cloud_notm}} users.
