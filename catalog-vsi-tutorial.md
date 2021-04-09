---

copyright:
  years: 2021
lastupdated: "2021-04-09"

keywords: onboard software, Terraform, virtual server image, virtual machine image, image, vm, vsi, validate, test, VSI image, VM image, private catalog

subcollection: account

content-type: tutorial
services: cloud-object-storage, vpc
account-plan: paid 

---

{:shortdesc: .shortdesc}
{:screen: .screen}  
{:codeblock: .codeblock}  
{:pre: .pre}
{:tip: .tip}
{:note: .note}
{:beta: .beta}
{:external: target="_blank" .external}
{:step: data-tutorial-type='step'} 


# Onboarding a sample virtual server image 
{: #catalog-vsi-tutorial}
{: toc-content-type="tutorial"}
{: toc-services="cloud-object-storage, vpc"} 

This tutorial walks you through how to onboard a sample virtual server image to a private catalog in your account. By completing this tutorial, you learn how to import a specific version, configure the  deployment details, validate that virtual server image can be installed on a deployment target, and share the virutal server image with users in your account. 
{: shortdesc}

This tutorial uses [sample Terraform code](https://github.com/IBM-Cloud/isv-vsi-product-deploy-sample){: external} to create a virtual server image. As you complete the tutorial, adapt each step to match your product's desired structure. 

## Before you begin
{: #catalog-vsi-prereqs}

1. Create an instance of [{{site.data.keyword.cloud_notm}} Object Storage](/docs/cloud-object-storage?topic=cloud-object-storage-getting-started-cloud-object-storage) and upload your image to a bucket.
2. Create your [{{site.data.keyword.cloud_notm}} Virtual Private Cloud](/docs/vpc?topic=vpc-getting-started). 
3. [Import your custom image to all regions](https://github.com/IBM-Cloud/isv-vsi-product-deploy-sample/tree/main#import-your-custom-image-to-all-supported-regions){: external} in which you want your software to be available. 
4. Create your [Terraform template](/docs/schematics?topic=schematics-create-tf-config). 
5. Upload your Terraform template to your GitHub repository. Use the [latest release of the sample Terraform code](https://github.com/IBM-Cloud/isv-vsi-product-deploy-sample/releases/tag/v1.0 ){: external} as an example of how to set up your repository. 
6. Make sure you're assigned the {{site.data.keyword.cloud_notm}} Identity and Access Management (IAM) editor role on the catalog management service. See [Assigning access to account management services](/docs/account?topic=account-account-services) for more information.

## Create a private catalog
{: #catalog-vsi-create}
{: step}

1. Go to **Manage** > **Catalogs**, and click **Create a catalog**. 
1. Select **Product default** as the catalog type. 
1. Enter the name of your catalog, for example, `Sample virtual server image catalog`.
1. Select **No products** to exclude all products in the {{site.data.keyword.cloud}} catalog from your catalog.
1. Click **Create**.

## Import the virtual server image to your private catalog
{: #catalog-vsi-import}
{: step}

1. From the Private products page, click **Add**.
4. Confirm that **Public repository** is selected as the repository type.
5. Enter `https://github.com/IBM-Cloud/isv-vsi-product-deploy-sample/releases/download/v1.0/isv-vsi-product-deploy-sample.tar.gz` as the URL of the public GitHub repository. 
6. Select **Compute / Virtual Machines** as the category type.
6. Accept the default value for **Version** field.
7. Select the **This Terraform template is a virtual server image** checkbox. 
8. Click **Add**.

## Configure the deployment details
{: #catalog-vsi-cfg-deployment}
{: step}

From the Configure product tab, configure the deployment values for the software installation.

1. Click **Add deployment values** in the Configure the deployment details section.
2. Select **Parameter** to select all options, and click **Add deployment values**.
3. Customize which parameters are required for users to specify during the installation and which ones are hidden from users altogether. For the purposes of this tutorial, configure each parameter as described in the following table.

| Parameter | Description | Required for users to specify? | Hidden from users? |
| --- | ---------- | --- | --- | 
| `TF_VERSION` | The version of the Terraform engine that's used in the Schematics workspace. | No | Yes |
| `image_name` | The name, with version specified, of the OS image that runs the virtual server instance. | No | Yes | 
| `region` | The region in which the VPC instance is located. | Yes | No |
| `ssh_key_name` | The name of the public SSH key to use when creating the virtual server instance. | Yes | No |
| `subnet_id` | The ID of the subnet within the VPC that the virtual server instance uses. | Yes | No |
| `vsi_instance_name` | The name of the virtual server instance. | Yes | No |
| `vsi_profile` | The profile of compute CPU and memory resources to use when creating the virtual server instance. | No | No |
| `vsi_security_group` | The name of the security group that is created. | Yes | No |
  
## Set the license requirements
{: #catalog-vsi-cfg-license}
{: step}

If users are required to accept any license agreements beyond the {{site.data.keyword.cloud_notm}} Services Agreement, provide the URL to each agreement. Or, if users can bring their own licenses, you can provide that URL as well.  

1. From the Add license tab, click **Add**. 
2. Enter the name and URL, and click **Update**.


## Validate the virtual server image
{: #catalog-vsi-validate}
{: step}

1. In the Configure Schematics workspace section, accept the default value that's displayed in the **Name** field. 
1. Enter the values for the parameters listed in the Deployment values section.
1. Click **Update**.
2. From the Validation summary panel, select **I have read and agree to the following license agreements**.
3. Click **Validate**.

## Update the visibility of the virtual server image to public 
{: #catalog-vsi-public}
{: step}

By default, the visibility of the virtual server image is private. After you validate it and {{site.data.keyword.cloud_notm}} has granted you access to run the command, you can use an API to make the image available for use. For more information, see [Update the visibility of your image](https://github.com/IBM-Cloud/isv-vsi-product-deploy-sample/tree/v1.0#update-the-visibility-of-your-image-patch-api){: external}.



