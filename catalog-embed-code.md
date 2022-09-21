---

copyright:
  years: 2022
lastupdated: "2022-09-19"

keywords: terraform, embed code

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Embedding software in Terraform
{: #catalog-embed-code}

Instead of deploying the product on {{site.data.keyword.cloud}}, you can copy and embed the product's code into your own Terraform configuration. This task is for users who are experienced with Terraform.
{: shortdesc}

## Before you begin
{: #embed-code-prereqs}

1. Install the [{{site.data.keyword.cloud_notm}} CLI](/docs/cli?topic=cli-install-ibmcloud-cli).
2. Install the [Catalog Management CLI plug-in](/docs/cli?topic=cli-manage-catalogs-plugin#install-managecatalogs).
3. Ensure that you have a Terraform environment on your local machine.

## Running locally in a Terraform template
{: #embed-code}

1. Log in to the {{site.data.keyword.cloud_notm}} CLI.
1. Copy the code from the {{site.data.keyword.cloud_notm}} catalog.
1. Embed the code in your Terraform template, and set the values for your configuration.
1. Run the `ibmcloud catalog netrc` command to configure a `.netrc` file with an authentication token.

   You might need to configure the {{site.data.keyword.cloud_notm}} provider. For more information, see the [{{site.data.keyword.cloud_notm}} Provider docs](https://registry.terraform.io/providers/IBM-Cloud/ibm/latest/docs){: external}.
   {: note}

1. Run the `terraform init` command to download all of the required Terraform modules.
1. Run the `terraform plan` command to see what resources will be created.
1. Run the `terraform apply` command to create the resources. It might take some time to create the resources.
