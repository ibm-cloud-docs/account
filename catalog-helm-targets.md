---

copyright:
  years: 2020, 2022
lastupdated: "2022-02-21"

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

You can deploy your Helm chart to a new target by using Terraform.

1. To install the Terraform CLI and configure the {{site.data.keyword.cloud_notm}} Provider plug-in for Terraform, follow the tutorial for [Getting started with Terraform on {{site.data.keyword.cloud}}](/docs/ibm-cloud-provider-for-terraform?topic=ibm-cloud-provider-for-terraform-getting-started). The plug-in abstracts the {{site.data.keyword.cloud_notm}} APIs that are used to complete this task.

2. Create a Terraform configuration file that is named `main.tf`. In this file, you add the configuration to update your deployment target by using HashiCorp Configuration Language. For more information, see the [Terraform documentation](https://www.terraform.io/docs/language/index.html){: external}.

   The following example shows the software version details by using the `cm_version` resource, where `offering_id` is used to identify the Helm chart.

   ```terraform
   resource "cm_version" "cm_version" {
   catalog_identifier = "catalog_identifier"
   offering_id = "offering_id"
   zipurl = "placeholder"
   }
   ```
   {: codeblock}

    You can specify `target_kinds` for the `cm_version` resource. For more information, see the argument details on the [Terraform Catalog Management](https://registry.terraform.io/providers/IBM-Cloud/ibm/latest/docs/resources/cm_version){: external} page.

3. Initialize the Terraform CLI.

   ```terraform
   terraform init
   ```
   {: pre}

4. Create a Terraform execution plan. The Terraform execution plan summarizes all the actions that need to be run to update the deployment target.

   ```terraform
   terraform plan
   ```
   {: pre}

5. Update the deployment target.

   ```terraform
   terraform apply
   ```
   {: pre}
