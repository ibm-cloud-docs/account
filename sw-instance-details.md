---


copyright:
  years: 2021
lastupdated: "2021-08-31"

keywords: software instance, logs, delete, resource list, operator, operator bundle

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:beta: .beta}
{:important: .important}
{:download: .download}
{:external: target="_blank" .external}
{:ui: .ph data-hd-interface='ui'}
{:cli: .ph data-hd-interface='cli'}
{:api: .ph data-hd-interface='api'}
{:terraform: .ph data-hd-interface='terraform'}

# Managing software instances
{: #sw-instance-details}

After you install an Operator from the {{site.data.keyword.cloud}} catalog, you can view details about it from your software instance details page. You can also take common actions such as renaming, deleting, and viewing the logs for the instance.  
{: shortdesc}

## Viewing details about your software instance in the console
{: #sw-view-details}
{: ui}

The details page for your software instance includes information about the installed version, deployment target, pricing plan, and so on. To view details about your software instance, complete the following steps: 

1. Go to the **Menu** icon ![Menu icon](../icons/icon_hamburger.svg "Menu") > **Resource list**. 
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

1. To install the Terraform CLI and configure the {{site.data.keyword.cloud_notm}} Provider plug-in for Terraform, follow the tutorial for [Getting started with Terraform on {{site.data.keyword.cloud_notm}}](/docs/ibm-cloud-provider-for-terraform?topic=ibm-cloud-provider-for-terraform-getting-started). The plug-in abstracts the {{site.data.keyword.cloud_notm}} APIs that are used to complete this task.

2. Create a Terraform configuration file that is named `main.tf`. In this file, you add the configuration to rename your software instance by using HashiCorp Configuration Language. For more information, see the [Terraform documentation](https://www.terraform.io/docs/language/index.html){: external}.

   The following example shows the software instance details by using the `ibm_cm_offering_instance` resource, where `label` is a display name to identify the instance. To rename your software instance, update `label`. 

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
  
3. Initialize the Terraform CLI.

   ```
   terraform init
   ```
   {: pre}
   
4. Create a Terraform execution plan. The Terraform execution plan summarizes all the actions that need to be run to rename the software instance.

   ```
   terraform plan
   ```
   {: pre}

5. Rename the software instance.

   ```
   terraform apply
   ```

## Deleting your software instance by using Terraform
{: #sw-delete-terraform}
{: terraform}

You can delete your software instance by using Terraform. 

1. To install the Terraform CLI and configure the {{site.data.keyword.cloud_notm}} Provider plug-in for Terraform, follow the tutorial for [Getting started with Terraform on {{site.data.keyword.cloud_notm}}](/docs/ibm-cloud-provider-for-terraform?topic=ibm-cloud-provider-for-terraform-getting-started). The plug-in abstracts the {{site.data.keyword.cloud_notm}} APIs that are used to complete this task.

2. Create a Terraform configuration file that is named `main.tf`. In this file, you add the configuration to delete your software instance by using HashiCorp Configuration Language. For more information, see the [Terraform documentation](https://www.terraform.io/docs/language/index.html){: external}.

3. You can delete the software instance by removing the following code block from your Terraform file. You must have provisioned the `cm_offering_instance` using the Terraform file.

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
  
3. Initialize the Terraform CLI.

   ```
   terraform init
   ```
   {: codeblock}
   
4. Create a Terraform execution plan. The Terraform execution plan summarizes all the actions that need to be run to delete the software instance.

   ```
   terraform plan
   ```
   {: codeblock}

5. Delete the software instance.

   ```
   terraform apply
   ```
   {: codeblock}
   
