---

copyright:
  years: 2022
lastupdated: "2022-06-14"

keywords:  terraform, run local, customize, cli

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Running products locally
{: #catalog-run-local}

Instead of deploying the product using the automated process from the catalog tile, you can manually deploy the solution locally. This user should be very familiar with Terraform.
{: shortdesc} 

## Before you begin
{: #run-local-prereqs}

Install the IBM Cloud CLI and the Catalog Management CLI plug-in.

## Installing from the CLI 
{: #local-install}

1. Copy into a file named `main.tf` and set the values for "environment_name" and "ibm_region". 
1. Configure .netrc file with authentication token for IBM Cloud: `ibmcloud catalog netrc`.
1. Export the value of your IBM Cloud API key for the IBM Terraform provider: `export IC_API_KEY=<your apiKey value>`. If you have not yet created an API key, see "Creating an API key" at https://cloud.ibm.com/docs/account?topic=account-userapikey&interface=ui#create_user_key.
1. Run the command `terraform init` to download all needed terraform modules. 
1. Run the command `terraform plan` to see what resources will be created. 
1. Run the command `terraform apply` to create the resources. This might take some time. 
 














