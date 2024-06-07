---

copyright:
  years: 2019, 2024
lastupdated: "2024-01-05"

keywords: catalog, private catalogs, account catalogs

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Creating private catalogs
{: #create-private-catalog}

The process to onboard software to your account includes importing a version to a private catalog, validating that the version can be successfully installed on the target infrastructure that you require, and publishing the software to your account. The software is then available to users in your account.
{: shortdesc}

## Before you begin
{: #prereq-create}

Verify that you're using a Pay-As-You-Go or Subscription account. See [Viewing your account type](/docs/account?topic=account-account_settings#view-acct-type) for more details.

## Creating a private catalog
{: #create-catalog-ui}
{: ui}

Private catalogs provide a way for you to manage access to products for users in your account.

1. Go to **Manage** > **Catalogs** in the {{site.data.keyword.cloud}} console, and click **Create a catalog**.
1. Enter a name and description of your catalog.
1. Select to exclude or include all products in the {{site.data.keyword.cloud_notm}} catalog in your private catalog. For more information about how this affects visibility in the catalog, see [Managing catalog settings](/docs/account?topic=account-filter-account&interface=ui).
1. Click **Create**.

## Creating a private catalog by using Terraform
{: #create-catalog-terraform}
{: terraform}

You can create a private catalog by using Terraform.

1. To install the Terraform CLI and configure the {{site.data.keyword.cloud_notm}} Provider plug-in for Terraform, follow the tutorial for [Getting started with Terraform on {{site.data.keyword.cloud}}](/docs/ibm-cloud-provider-for-terraform?topic=ibm-cloud-provider-for-terraform-getting-started). The plug-in abstracts the {{site.data.keyword.cloud_notm}} APIs that are used to complete this task.

2. Create a Terraform configuration file that is named `main.tf`. In this file, you add the configuration to create a private catalog by using HashiCorp Configuration Language. For more information, see the [Terraform documentation](https://developer.hashicorp.com/terraform/language){: external}.

   The following example creates a private catalog by using the `ibm_cm_catalog` resource, where `label` is a display name to identify the catalog.

   ```terraform
   resource "ibm_cm_catalog" "cm_catalog" {
   label = "label"
   short_description = "short_description"
   }
   ```
   {: codeblock}

   For more information, see the argument reference details on the [Terraform Catalog Management](https://registry.terraform.io/providers/IBM-Cloud/ibm/latest/docs/resources/cm_catalog){: external} page.

3. Initialize the Terraform CLI.

   ```terraform
   terraform init
   ```
   {: pre}

4. Run `terraform plan` to generate a Terraform execution plan to preview the proposed actions. The Terraform execution plan summarizes all the actions that need to be run to create the catalog.

   ```terraform
   terraform plan
   ```
   {: pre}

5. Create the catalog.

   ```terraform
   terraform apply
   ```
   {: pre}
