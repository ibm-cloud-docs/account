---


copyright:

  years: 2021, 2025
lastupdated: "2025-01-28"

keywords: software instance, logs, delete, resource list, operator, operator bundle

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Managing software instances
{: #sw-instance-details}

After you install an Operator from the {{site.data.keyword.cloud}} catalog, you can view details about it from your software instance details page. You can also take common actions such as renaming, deleting, and viewing the logs for the instance.
{: shortdesc}

## Viewing details about your software instance in the console
{: #sw-view-details}
{: ui}

The details page for your software instance includes information about the installed version, deployment target, pricing plan, and so on. To view details about your software instance, complete the following steps:

1. Go to the **Navigation Menu** icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Resource list**.
1. Expand **Services and software**.
1. Click the name of your software instance.

## Viewing logs for your software instance in the console
{: #sw-view-logs}
{: ui}

To view changes to your software instance, click **Actions** > **View logs**.

## Renaming your software instance in the console
{: #sw-rename}
{: ui}

To rename your software instance, click **Actions** > **Rename instance**.

## Deleting your software instance in the console
{: #sw-delete}
{: ui}

Deleting a software instance removes the software from the cluster to which it is deployed. To delete your software instance, click **Actions** > **Delete instance**.

## Before you begin
{: #sw-instance-details-tf}
{: terraform}

Before you can rename your software instance by using Terraform, make sure that you have completed the following:

- Install the Terraform CLI and configure the {{site.data.keyword.cloud_notm}} Provider plug-in for Terraform. For more information, see the tutorial for [Getting started with Terraform on {{site.data.keyword.cloud}}](/docs/ibm-cloud-provider-for-terraform?topic=ibm-cloud-provider-for-terraform-getting-started). The plug-in abstracts the {{site.data.keyword.cloud_notm}} APIs that are used to complete this task.
- Create a Terraform configuration file that is named `main.tf`. In this file, you define resources by using HashiCorp Configuration Language. For more information, see the [Terraform documentation](https://developer.hashicorp.com/terraform/language){: external}.

## Viewing details about your software instance by using Terraform
{: #viewing-sw-instance-terraform}
{: terraform}

You can't view details about your software instance by using Terraform. To view your software instance details, switch to the UI steps.

## Viewing logs for your software instance by using Terraform
{: #sw-view-logs-terraform}
{: terraform}

You can't view logs for your software instance by using Terraform. To view the logs, switch to the UI steps.

## Renaming your software instance by using Terraform
{: #sw-rename-terraform}
{: terraform}

You can rename your software instance by using Terraform.

1. Create an argument in your `main.tf` file. The following example shows the software instance details by using the `ibm_cm_offering_instance` resource, where `label` is a display name to identify the instance. To rename your software instance, update `label`.

   ```terraform
   resource "ibm_cm_offering_instance" "cm_offering_instance" {
   catalog_id = "catalog_id"
   label = "label"
   kind_format = "operator"
   version = "version"
   cluster_id = "cluster_id"
   cluster_region = "cluster_region"
   cluster_namespaces = [ "cluster_namespaces", "cluster_namespaces" ]
   cluster_all_namespaces = false
   }
   ```
   {: codeblock}

    You can specify an `update` timeout for the `ibm_cm_offering_instance` resource. For more information, see the timeout reference details on the [Terraform Catalog Management](https://registry.terraform.io/providers/IBM-Cloud/ibm/latest/docs/resources/cm_offering_instance#timeouts){: external} page.

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


## Deleting your software instance by using Terraform
{: #sw-delete-terraform}
{: terraform}

You can delete your software instance by using Terraform.

1. You can delete the software instance by removing the following code block from your Terraform file. You must have created the `cm_offering_instance` using the Terraform file.

   ```terraform
   resource "ibm_cm_offering_instance" "cm_offering_instance" {
   catalog_id = "catalog_id"
   label = "label"
   kind_format = "operator"
   version = "version"
   cluster_id = "cluster_id"
   cluster_region = "cluster_region"
   cluster_namespaces = [ "cluster_namespaces", "cluster_namespaces"]
   cluster_all_namespaces = false
   }
   ```
   {: codeblock}

   You can specify a `delete` timeout for the `ibm_cm_offering_instance` resource. For more information, see the timeout reference details on the [Terraform Catalog Management](https://registry.terraform.io/providers/IBM-Cloud/ibm/latest/docs/resources/cm_offering_instance#timeouts){: external} page.

1. Initialize the Terraform CLI.

   ```terraform
   terraform init
   ```
   {: pre}

1. Run `terraform plan` to generate a Terraform execution plan to preview the proposed actions. The Terraform execution plan summarizes all the actions that need to be run to delete the software instance.

   ```terraform
   terraform plan
   ```
   {: pre}

1. Delete the software instance.

   ```terraform
   terraform apply
   ```
   {: pre}
