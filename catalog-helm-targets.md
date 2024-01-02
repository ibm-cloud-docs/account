---

copyright:
  years: 2020, 2024
lastupdated: "2024-01-02"

keywords: onboard software, Helm chart, software, private catalog, target, deployment target

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Deploying a Helm chart to a new target
{: #helm-targets}

You can copy the configuration of an existing version of a Helm chart and deploy it to a new deployment target. The deployment target options for Helm charts are {{site.data.keyword.containerlong_notm}} and {{site.data.keyword.openshiftlong_notm}}.
{: shortdesc}

## Deploying a Helm chart to a new target using the console
{: #helm-targets-ui}
{: ui}

1. Go to the **Manage** > **Catalogs** in the {{site.data.keyword.cloud}} console, and click **Private catalogs**.
1. Select the private catalog that contains the current Helm chart version.
1. Click the existing version from the list of products in your private catalog.
1. Click **Add version** from the Version list table.
1. Select **Copy the configuration of an existing version and deploy it to a new target.**
1. Select your existing version.
1. Click **Copy existing version**.

Your copied version is displayed in your version list as a separate entry from your existing version. The two versions have the same version number but different deployment targets.

## Deploying a Helm chart to a new target by using Terraform
{: #helm-targets-tf}
{: terraform}

Before you can deploy a Helm chart to a new target by using Terraform, make sure that you have completed the following:

- Install the Terraform CLI and configure the {{site.data.keyword.cloud_notm}} Provider plug-in for Terraform. For more information, see the tutorial for [Getting started with Terraform on {{site.data.keyword.cloud}}](/docs/ibm-cloud-provider-for-terraform?topic=ibm-cloud-provider-for-terraform-getting-started). The plug-in abstracts the {{site.data.keyword.cloud_notm}} APIs that are used to complete this task.
- Create a Terraform configuration file that is named `main.tf`. In this file, you define resources by using HashiCorp Configuration Language. For more information, see the [Terraform documentation](https://www.terraform.io/docs/language/index.html){: external}.

Use the following steps to deploy your Helm chart to a new target by using Terraform:

1. Create an argument in your `main.tf` file. The following example shows the software version details by using the `cm_version` resource, where `offering_id` is used to identify the Helm chart.

   ```terraform
   resource "cm_version" "cm_version" {
   catalog_identifier = "catalog_identifier"
   offering_id = "offering_id"
   zipurl = "placeholder"
   }
   ```
   {: codeblock}

    You can specify `target_kinds` for the `cm_version` resource. For more information, see the argument details on the [Terraform Catalog Management](https://registry.terraform.io/providers/IBM-Cloud/ibm/latest/docs/resources/cm_version){: external} page.

1. After you finish building your configuration file, initialize the Terraform CLI. For more information, see [Initializing Working Directories](https://developer.hashicorp.com/terraform/cli/init){: external}.

   ```terraform
   terraform init
   ```
   {: pre}

1. Provision the resources from the `main.tf` file. For more information, see [Provisioning Infrastructure with Terraform](https://developer.hashicorp.com/terraform/cli/run){: external}.

   1. Run `terraform plan` to generate a Terraform execution plan to preview the proposed actions.

      ```terraform
      terraform plan
      ```
      {: pre}

   1. Run `terraform apply` to create the resources that are defined in the plan.

      ```terraform
      terraform apply
      ```
      {: pre}
